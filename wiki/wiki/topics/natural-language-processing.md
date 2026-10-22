---
type: topic
title: "Natural language processing"
summary: "Methods that score firm text. Dictionary sentiment, similarity to a reference narrative, and topic models are entries here."
created: 2026-10-22
updated: 2026-10-22
tags: [natural-language-processing, narrative]
sources: [wiki/sources/2024-06-01-flynn-sastry-macroeconomics-of-narratives.md]
---

# Natural language processing

Dictionary sentiment, tf-idf narrative scoring, and latent Dirichlet allocation are entries here, not separate concepts.

## How the text is measured

- Flynn and Sastry. The corpora are SEC Forms 10-K from 1995 to 2018 and sales and earnings calls from 2002 to 2014. Processing keeps English tokens, lemmatizes them, and groups co-occurring pairs into bigrams. Each document becomes a vector of term counts. The 10-K sample has 100,936 firm-years. The call sample has 25,589 firm-years. Source: [The Macroeconomics of Narratives](../sources/2024-06-01-flynn-sastry-macroeconomics-of-narratives.md).
- Dictionary sentiment uses the Loughran and McDonald positive and negative word lists. Positive and negative intensities are term frequencies. Net sentiment is the difference of their z-scores. A firm is optimistic in a year when its net sentiment is at or above the sample median. The same construction is applied to earnings calls. Source: [The Macroeconomics of Narratives](../sources/2024-06-01-flynn-sastry-macroeconomics-of-narratives.md).
- tf-idf narrative scoring compares each 10-K with the chapter of Shiller's *Narrative Economics* that describes one of nine perennial economic narratives. A word scores highly when it is common in that chapter and rare across 10-Ks. The narrative score is the document's frequency of the top 100 such words, and adoption is above-median frequency. Source: [The Macroeconomics of Narratives](../sources/2024-06-01-flynn-sastry-macroeconomics-of-narratives.md).
- Latent Dirichlet allocation treats each 10-K as a mixture of \(K=100\) topics and each topic as a distribution over words. The model is estimated by variational Bayes on a random 10,000 of 37,684 firms, then used to score every document. A firm adopts a topic when its posterior topic probability is above the sample median. Source: [The Macroeconomics of Narratives](../sources/2024-06-01-flynn-sastry-macroeconomics-of-narratives.md).

## What the measurement identifies

- Above-median sentiment predicts 3.6 percentage points more hiring inside industry-year cells. The coefficient is 3.1 percentage points with current and lagged productivity and lagged employment, and 2.5 percentage points with book-to-market, the stock return, and leverage. Earnings-call sentiment produces a similar hiring coefficient. Deciles of the continuous score line up monotonically with hiring. Source: [The Macroeconomics of Narratives](../sources/2024-06-01-flynn-sastry-macroeconomics-of-narratives.md).
- The same optimism indicator predicts lower subsequent stock returns and profitability. It predicts sales guidance that exceeds realized sales: the coefficient on an above-median guidance error is 0.056 once productivity and employment controls are included. Future TFP growth is not higher. A firm that is doing well today is more likely to be optimistic later. Source: [The Macroeconomics of Narratives](../sources/2024-06-01-flynn-sastry-macroeconomics-of-narratives.md).
- A post-LASSO of the optimism indicator on the nine Shiller scores and the one hundred topics keeps eight Shiller narratives and thirty topics. Those selected series are the granular narratives whose contagion, association, and stubbornness are estimated one by one. Source: [The Macroeconomics of Narratives](../sources/2024-06-01-flynn-sastry-macroeconomics-of-narratives.md).

## Problems and mitigations

- The Loughran–McDonald lists score tone in financial filings. Words such as "liability" are classified from their use in 10-Ks. The mapping from that tone to a prior about mean productivity is the model's interpretation of the indicator. Source: [The Macroeconomics of Narratives](../sources/2024-06-01-flynn-sastry-macroeconomics-of-narratives.md).
- The binary indicator is an in-sample median split. Replacing it with deciles of the continuous score preserves the hiring gradient. Using the continuous sentiment series in the spread regression preserves stubbornness, contagion, and association. Source: [The Macroeconomics of Narratives](../sources/2024-06-01-flynn-sastry-macroeconomics-of-narratives.md).
- The tf-idf scores inherit the wording of Shiller's chapters. The topic model does not use that wording. Its topic count is set at 100, and the Dirichlet posteriors are estimated on a subset of firms. The post-LASSO step then drops the scores that do not predict the optimism indicator. Source: [The Macroeconomics of Narratives](../sources/2024-06-01-flynn-sastry-macroeconomics-of-narratives.md).
