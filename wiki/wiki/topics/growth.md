---
type: topic
title: "Growth"
summary: "What generates sustained growth of output and productivity, and how large that contribution is in the data."
created: 2026-10-16
updated: 2026-10-16
tags: [growth, production-network]
sources: [wiki/sources/2020-01-01-acemoglu-azar-endogenous-production-networks.md]
---

# Growth

## How growth is modelled

- Acemoglu and Azar. One new product arrives each period. With \(n\) products already available, one more product raises each existing industry's input combinations from \(2^{n-1}\) to \(2^n\). Firms adopt the cost-minimizing combination at no cost. New goods have vanishing consumption shares, so the growth is the selection of cheaper input combinations, transmitted through the Leontief inverse of the [production network](../concepts/production-network.md). Log productivities of input sets are drawn so that the best set for each industry grows asymptotically at rate \(D > 0\). Source: [Endogenous Production Networks](../sources/2020-01-01-acemoglu-azar-endogenous-production-networks.md).

## Results

- The asymptotic growth rate of real GDP is \(g^\ast = D\sum_{i,j}\beta_i\mathcal{L}_{ij} > 0\) almost surely. A finite set of industries that can choose their suppliers is enough for \(g^\ast > 0\). If each firm may keep only its current technique or one randomly drawn alternative, sustained growth disappears. Growth remains when, in some categories, new inputs replace old ones. Source: [Endogenous Production Networks](../sources/2020-01-01-acemoglu-azar-endogenous-production-networks.md).
- On BEA data for 488 industries, 1987–2007, a dummy for a Jaccard distance of the input set above that year's 20th percentile has coefficient 0.018 on five-year TFP growth (standard error 0.007). The implied contribution is 0.42 percentage points, about 40 percent of the 1.05 percent annualized average industry TFP growth. Excluding computers, the contribution is 0.25 percentage points. Source: [Endogenous Production Networks](../sources/2020-01-01-acemoglu-azar-endogenous-production-networks.md).

## Problems and mitigations

- The tail condition that delivers \(D > 0\) holds for Gumbel and exponential draws. Finite and normal distributions have thinner tails, and Pareto and Fréchet distributions have thicker tails, so they fall outside the theorem. Late goods are also kept from taking a large share of costs. The creative-destruction extension allows new inputs to replace old ones in some categories and still gives \(g^\ast > 0\). Source: [Endogenous Production Networks](../sources/2020-01-01-acemoglu-azar-endogenous-production-networks.md).
- The TFP regression is illustrative. Sectors that become more productive for other reasons may also add inputs, so the coefficient can be biased upward. No later source in the wiki yet replaces that regression.
