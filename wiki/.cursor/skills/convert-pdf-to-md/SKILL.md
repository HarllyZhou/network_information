---
name: convert-pdf-to-markdown
description: >-
  Convert an academic PDF to markdown by locating text, tables, figures, and
  math, then extracting each in its own format. Use when the user asks to
  convert a PDF to markdown or MD, says "convert this pdf to md", "convert
  this paper to markdown", "extract the main body", or wants equations, tables,
  and figures preserved. Use the PDF text layer for born-digital papers. Use
  Marker only when the text layer is missing or garbage.
---

# Convert PDF to Markdown

## Goal

Locate text, tables, figures, and math. Then extract each region in its own format. Do not send a born-digital paper through Marker.

Default:

- Read the PDF text layer first.
- Exclude the appendix. Keep the references.
- Write markdown beside the PDF.
- Write figure images under `raw/assets/<pdf-stem>/`.
- Keep scratch files under `scripts/temporary/<pdf-stem>/`.

Paths are relative to the wiki root, the directory that contains `raw/` and `scripts/`.

## When to Use

Use this skill when the user asks to convert a PDF to markdown, extract a paper's main body, or redo a conversion whose equations, tables, or figures came out as prose.

## Rules

- Before any command or edit, report the plan and wait for `proceed`.
- Do not install or import Marker until the text-layer check says the PDF is a scan or the text is garbage.
- On a born-digital PDF, do not OCR, do not chunk, and do not use the GPU.
- An appendix starts only when a page's first content heading is `Appendix`, `Online Appendix`, `Technical Appendix`, or `Data Appendix`. A mention inside a paragraph is not an appendix.
- Do not delete the final markdown unless the user asks.
- Remove a stale incomplete output folder before a fresh rerun.

## Workflow

### 1. Decide the path

Open the PDF with `pypdfium2`. For each page, count extracted characters and the share of control characters (`\x02`), replacement characters, and private-use characters.

Born-digital when the median page has more than about 400 characters and that share is low. Otherwise treat it as a scan and use [Scan fallback](#scan-fallback).

### 2. Locate regions

Do this before writing the markdown. Record page index and bounding box for every region. Save the map at `scripts/temporary/<pdf-stem>/regions.json` and print the counts.

Group text objects into blocks. Label each block as one of:

- `heading` — larger type, or a line such as `I. Data` or `REFERENCES`
- `body` — prose
- `caption` — begins with `Table`, `Figure`, or `Notes:`
- `footnote` — smaller type at the bottom, or a line that starts with a footnote number

Tables come from `pdfplumber` `find_tables()`, not from the body text. A table bbox is not also a body block.

Figures are embedded images and large vector drawings. Attach the nearest `Figure N` caption. A small logo or journal rule is not a figure.

Math is separate from body text:

- `display` — a centered line, a run in a math font, or a line with an equation number `(N)` at the right margin
- `inline` — a math-font run inside a body block

Math fonts include names containing `Math`, `CMMI`, `CMSY`, `CMEX`, `Symbol`, or `Mathematical`. A line of operators (`=`, `∑`, fractions, subscripts) is math even when the font name is ordinary, if it is not a sentence.

Print: pages, body blocks, headings, tables, figures, display equations, inline runs, and the appendix start page or `none`.

### 3. Extract each region in its format

Walk regions in reading order: page, then top to bottom.

**Text.** Join wrapped lines into paragraphs. Delete soft hyphens (`\x02` and `\u00ad`) instead of leaving a broken word. Drop the running header and the bare page number. Break a paragraph when a short line ends with punctuation. Keep footnotes out of the next paragraph: emit them as `[^n]` at the marker and list them after the paragraph. Headings become `##` lines.

**Tables.** Extract each `pdfplumber` table as a markdown table. Put its caption on the line above. Do not flatten cells into a sentence.

**Figures.** Extract an embedded image's bytes when they exist. Otherwise render that bbox to PNG. Write `raw/assets/<pdf-stem>/figure-<page>-<n>.png` and insert `![caption](../assets/<pdf-stem>/figure-<page>-<n>.png)`. Do not OCR the figure.

**Math.** Emit LaTeX. Display equations are `$$...$$`, with `, \tag{N}` or `. \tag{N}` when the PDF shows an equation number. Inline runs are `$...$`. Build the LaTeX from the text layer and, when Unicode is wrong, from the glyph name. Hangul, private-use, or control characters inside a symbol are a bad ToUnicode map, not the symbol itself. Record every glyph-name reconstruction. Do not OCR the page to recover one symbol.

Leave a region as plain text only when its structure is ambiguous, and list it in the report.

### 4. Assemble

Write `<pdf-stem>.md` beside the PDF. Stop before the appendix heading. Include references. Interleave text, tables, figures, and equations in reading order.

## Scan fallback

Use this only when step 1 says the text layer is missing or garbage.

- Do not use Marker 2 unless `llama-server` is on `PATH`.
- On macOS set `TORCH_DEVICE=cpu`. Do not run recognition on MPS; it hangs in Metal with no output file.
- Probe pages `0-4` with Marker 1.x, `--disable_multiprocessing`, and `--output_format markdown`. Marker 1.10 and Marker 2 have no `--disable_ocr` flag. Do not pass it.
- If three minutes pass with no markdown file and no progress past the current recognition count, kill the process and stop. Report the command. Do not start later chunks.
- Chunk the remaining pages, about five pages at a time, only after the probe writes a markdown file.
- On Marker output only, repair detached equation numbers and `<sup>` debris as in [Marker math cleanup](#marker-math-cleanup).

## Marker math cleanup

Apply this only to the scan fallback. Display equations that already contain `\tag{N}` stay as they are.

- A display equation followed by a line that is only `(N)`: delete that line and append `, \tag{N}` or `. \tag{N}` to the equation. Do not add a second comma or period.
- A line that is only `$$(N)$$`: fold `\tag{N}` into the preceding display.
- `. (N)$$` becomes `. \tag{N}$$`. `,\tag{N}` and `.\tag{N}` become `, \tag{N}` and `. \tag{N}`.
- `<sup>` used as a script becomes `$...$`: `g<sup>i</sup>` → `$g_i$`.
- After repair, the file should contain no `<sup>` tags and no equation number sitting outside its display.

## Report

Report only:

- path used: text layer or Marker
- appendix start page, or none
- counts of body blocks, tables, figures, display equations, and inline math
- final markdown path and figure directory
- glyph-name reconstructions
- regions left as plain text, and why
- for a Marker run: whether the probe was killed, and whether temp chunks were kept
