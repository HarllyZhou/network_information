---
type: source
title: "Flynn and Sastry, The Macroeconomics of Narratives (2024)"
summary: "Contagious priors about productivity move hiring and output. Measured optimism spreads across firms and accounts for part of two US recessions."
created: 2026-10-22
updated: 2026-10-22
tags: [narrative, contagion-of-beliefs, natural-language-processing, information-friction]
raw: raw/papers/2024-06-01-flynn-sastry-macroeconomics-of-narratives.pdf
---

# Flynn and Sastry, The Macroeconomics of Narratives (2024)

## Bibliographic

- Authors: Joel P. Flynn and Karthik Sastry
- Venue: NBER Working Paper 32602
- Date: 2024-06
- Raw file: `raw/papers/2024-06-01-flynn-sastry-macroeconomics-of-narratives.pdf`

## Key claims

1. A [narrative](../concepts/narrative.md) is a prior about aggregate productivity. Firms place weight on an optimistic mean \(\mu_O\) or a pessimistic mean \(\mu_P\) and combine that prior with a private Gaussian signal. Feeds [information friction](../topics/information-friction.md).
2. Narratives spread by contagion, which depends on how common the narrative already is, and by association, which depends on current output. The linear rule uses stubbornness \(u\), associativeness \(r\), and contagiousness \(s\). Feeds [contagion of beliefs](../topics/contagion-of-beliefs.md).
3. There is a unique quasi-loglinear equilibrium. Log output is linear in productivity and separable in the optimistic share \(Q_t\). Moving from full pessimism to full optimism changes log output by \(\alpha\delta^{OP}/(1-\omega)\). If contagion and this multiplier are large enough, unanimous optimism and unanimous pessimism are both stable. Feeds [narrative](../concepts/narrative.md) and [contagion of beliefs](../topics/contagion-of-beliefs.md).
4. A higher signal-to-noise ratio \(\kappa\) shrinks the output effect of narratives. When strategic complementarity is positive, that shrinkage is weakest at low \(\kappa\), where narratives are already strong. Feeds [information friction](../topics/information-friction.md).
5. Optimism is above-median Loughran–McDonald sentiment in 10-Ks and earnings calls. Shiller's nine perennial narratives are scored by tf-idf against his chapters. One hundred topics come from latent Dirichlet allocation. Feeds [natural language processing](../topics/natural-language-processing.md).
6. Optimistic firms hire about 3.6 percentage points more. The same language predicts lower future stock returns and profitability, and sales guidance that exceeds realizations. Feeds [narrative](../concepts/narrative.md), [contagion of beliefs](../topics/contagion-of-beliefs.md), and [natural language processing](../topics/natural-language-processing.md).
7. In the 10-K panel, next year's optimism loads on the firm's own lag (\(u=0.21\)), last year's average optimism (\(s=0.29\)), and real GDP growth (\(r=0.80\)). Feeds [contagion of beliefs](../topics/contagion-of-beliefs.md).
8. Measured optimism accounts for 32 percent of the output loss in 2000–2002, 18 percent in 2007–2009, and 19 percent of output variance. The hysteresis statistic for aggregate optimism is negative. Many granular narratives sit at or above the virality threshold, and optimism built from them still explains about 16 percent of output variance. Feeds [contagion of beliefs](../topics/contagion-of-beliefs.md).

## Figures and data

- SEC Forms 10-K, 1995–2018, 100,936 firm-years after processing, linked to Compustat. Earnings-call transcripts, 2002–2014, 25,589 firm-years. Managerial sales guidance from IBES. Real GDP from the national accounts, band-pass filtered.
- Table 1: optimism and hiring. Table 2: optimism and guidance that exceeds realized sales. Table 3: stubbornness, contagion, and association. Table 5: calibration.
- Figure 4: optimism and future TFP growth, stock returns, and profitability. Figure 5: the contribution of optimism to cyclical GDP. Figure 6: the share of output variance and autocovariance attributed to optimism. Figure 8: virality of the granular narratives.

## Pages updated

- [Narrative](../concepts/narrative.md) (created)
- [Contagion of beliefs](../topics/contagion-of-beliefs.md) (created)
- [Natural language processing](../topics/natural-language-processing.md) (created)
- [Information friction](../topics/information-friction.md) (updated)
