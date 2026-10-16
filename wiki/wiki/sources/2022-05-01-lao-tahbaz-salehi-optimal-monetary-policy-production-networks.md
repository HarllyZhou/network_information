---
type: source
title: "La'O and Tahbaz-Salehi, Optimal Monetary Policy in Production Networks (2022)"
summary: "The input-output matrix is a parameter. Optimal policy stabilizes a price index that puts more weight on larger, stickier, and more upstream industries."
created: 2026-10-16
updated: 2026-10-16
tags: [production-network, monetary-policy, nominal-rigidity]
raw: raw/papers/2022-05-01-lao-tahbaz-salehi-optimal-monetary-policy-production-networks.pdf
---

# La'O and Tahbaz-Salehi, Optimal Monetary Policy in Production Networks (2022)

## Bibliographic

- Authors: Jennifer La'O and Alireza Tahbaz-Salehi
- Venue: Econometrica 90 (3): 1295–1336
- Date: 2022-05
- Raw file: `raw/papers/2022-05-01-lao-tahbaz-salehi-optimal-monetary-policy-production-networks.pdf`

## Key claims

1. The [production network](../concepts/production-network.md) is given. Firm \(k\) in industry \(i\) produces \(y_{ik} = z_i \zeta_i \ell_{ik}^{\alpha_i} \prod_j x_{ij,k}^{a_{ij}}\), with \(\alpha_i + \sum_j a_{ij} = 1\). The input–output matrix \(A = [a_{ij}]\) and the Leontief inverse \(\mathcal{L} = (I - A)^{-1}\) are parameters of technology. Firms do not choose their supplier sets.
2. Nominal rigidities are information frictions. Firms set nominal prices from private signals about productivity and do not observe the aggregate state. Sticky information, in which a fraction of firms see the shocks and the rest price from the prior, is a special case. Quantities are chosen after prices and productivities are observed. Industry revenue taxes are non-contingent and are set to remove steady-state markups, so the flexible-price equilibrium is efficient. [Monetary policy](../concepts/monetary-policy.md) sets nominal aggregate demand \(m\) in the cash-in-advance constraint \(PC = m\). Feeds [optimal monetary policy](../topics/optimal-monetary-policy.md) and [information friction](../topics/information-friction.md).
3. A flexible-price allocation is implementable under sticky prices if and only if some nominal-wage function makes every firm's nominal marginal cost measurable with respect to its information (Theorem 1). For a generic information structure, no monetary policy implements a flexible-price allocation or the first best (Corollaries 1 and 2). If only one industry has sticky prices, stabilizing that industry's price implements any flexible-price allocation (Corollary 3). Feeds [optimal monetary policy](../topics/optimal-monetary-policy.md).
4. On the Cobb–Douglas network, upstream price flexibility is \(\rho_i = 1 - \sum_j a_{ij}(1 - \phi_j\rho_j)\), or \(\rho = (I - A\Phi)^{-1}\alpha\). The pass-through of nominal demand into consumption is \((1 - \rho_0) / (1 + (\gamma - 1 + 1/\eta)\rho_0)\), with \(\rho_0 = \beta'\Phi(I - A\Phi)^{-1}\alpha\). Feeds [network propagation](../topics/network-propagation.md).
5. The optimal policy stabilizes \(\sum_i \psi_i^\ast \log p_i = 0\). The weight on industry \(i\) is the sum of an output-gap term, a within-industry price-dispersion term, and an across-industry misallocation term. It is larger for industries that are larger in Domar weight, stickier, and more upstream, and for industries whose upstream suppliers are less sticky and whose downstream customers are stickier (Theorem 2). Feeds [optimal monetary policy](../topics/optimal-monetary-policy.md).
6. In a 66-industry calibration to the 2019 BEA input–output table, Pastén, Schoenle, and Weber price-change frequencies, and ILPA productivities for 1987–2019, the optimal policy leaves a welfare loss of 0.65 percent of quarterly consumption relative to flexible prices. Output-gap stabilization loses 0.67 percent. A consumption-share index loses 1.85 percent, a Domar-weight index 1.59 percent, and a stickiness-adjusted consumption index that ignores input–output linkages 1.46 percent. Feeds [optimal monetary policy](../topics/optimal-monetary-policy.md).

## Figures and data

- Table I: expected welfare loss under the optimal policy and four alternative price indexes, as a percent of steady-state consumption.
- Figure 3: sectoral weights in the optimal index and in the output-gap index. Both place the largest weight on the nominal wage.
- Calibration: 66 industries after dropping government. Quarterly price flexibility \(\phi_i = 1 - e^{-3 \times \mathrm{FPA}_i}\). Wage flexibility \(\phi_w = 0.30\). Within-industry elasticity \(\theta = 6\), Frisch elasticity \(\eta = 2\), and \(\gamma = 0.1\).

## Pages updated

- [Production network](../concepts/production-network.md) (updated)
- [Monetary policy](../concepts/monetary-policy.md) (created)
- [Optimal monetary policy](../topics/optimal-monetary-policy.md) (created)
- [Network propagation](../topics/network-propagation.md) (created)
- [Information friction](../topics/information-friction.md) (updated)
