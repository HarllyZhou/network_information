---
type: source
title: "Acemoglu and Azar, Endogenous Production Networks (2020)"
summary: "Firms choose their input sets. That choice lowers prices, can densify the network, and can sustain growth from new combinations."
created: 2026-10-16
updated: 2026-10-16
tags: [production-network, network-formation, growth]
raw: raw/papers/2020-01-01-acemoglu-azar-endogenous-production-networks.pdf
---

# Acemoglu and Azar, Endogenous Production Networks (2020)

## Bibliographic

- Authors: Daron Acemoglu and Pablo D. Azar
- Venue: Econometrica 88 (1): 33–82
- Date: 2020-01
- Raw file: `raw/papers/2020-01-01-acemoglu-azar-endogenous-production-networks.pdf`

## Key claims

1. Each contestable industry chooses a supplier set \(S_i\). Output is \(Y_i = F_i(S_i, A_i(S_i), L_i, X_i)\), with constant returns in labor and intermediates. The wage is the numeraire. Equilibrium price equals distorted unit cost, \(P_i^\ast = (1+\mu_i)K_i(S_i^\ast, A_i(S_i^\ast), P^\ast)\). The collection \(S^\ast\) is the [production network](../concepts/production-network.md). Feeds [network formation](../topics/network-formation.md).
2. With Hicks-neutral Cobb–Douglas technology, \(K_i = A_i(S_i)^{-1}\prod_{j\in S_i} P_j^{\alpha_{ij}}\) and \(p^\ast = -\mathcal{L}(S^\ast)\bigl(a(S^\ast) - m\bigr)\), where \(\mathcal{L}(S^\ast) = (I - \alpha(S^\ast))^{-1}\) and \(m_i = \log(1+\mu_i)\). An equilibrium exists. Prices are unique, and the network is generically unique. Zero distortions make the equilibrium Pareto efficient. Feeds [network formation](../topics/network-formation.md).
3. A better technology, or a lower distortion, weakly reduces every price. Under the technology–price single-crossing condition it also weakly expands every supplier set. A small productivity change can jump GDP and the network because adoption is discrete and one industry's price enters other industries' choices. Feeds [network formation](../topics/network-formation.md) and [network propagation](../topics/network-propagation.md).
4. One new product raises each existing industry's input combinations from \(2^{n-1}\) to \(2^n\). Selection of the cost-minimizing combination produces sustained growth, \(g^\ast = D\sum_{i,j}\beta_i\mathcal{L}_{ij} > 0\) almost surely. New goods have vanishing consumption shares. Feeds [growth](../topics/growth.md).
5. With Gumbel productivity draws, the probability that \(j\) supplies \(i\) is a logit in \(b_j\) and \(P_j\). Normalized indegrees collapse toward zero, while outdegrees stay dispersed. Feeds [network formation](../topics/network-formation.md).
6. On BEA data for 488 industries, 1987–2007, industries whose input set moves by more than that year's 20th-percentile Jaccard distance have 1.8 percentage points higher TFP growth (standard error 0.007). The implied contribution is 0.42 percentage points, about 40 percent of the 1.05 percent annualized average industry TFP growth. Feeds [growth](../topics/growth.md).

## Figures and data

- Figure 1: average number of suppliers in the harmonized U.S. commodity-by-commodity table, 61 industries, from under 50 in 1963 to more than 57 in 1996.
- Figure 2: a small productivity shock to one industry cascades to the complete network.
- Table I: five-year TFP growth on a Jaccard-distance dummy, 488 industries, 1987–2007.
- Calibration: 2007 U.S. input–output table, 391 sectors, with markups from De Loecker, Eeckhout, and Unger (2018). A 1 percent TFP increase in NAICS 334 adds 288 edges and raises real GDP by 0.72 percent.

## Pages updated

- [Production network](../concepts/production-network.md) (created)
- [Network formation](../topics/network-formation.md) (created)
- [Growth](../topics/growth.md) (created)
- [Network propagation](../topics/network-propagation.md) (updated)
