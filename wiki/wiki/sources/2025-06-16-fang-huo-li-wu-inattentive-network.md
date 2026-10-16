---
type: source
title: "Fang, Huo, Li, and Wu, Inattentive Network (2025)"
summary: "Firms browse suppliers that are closer and more volatile. Elastic attention makes price flexibility respond to policy."
created: 2026-10-16
updated: 2026-10-16
tags: [information-friction, production-network, monetary-policy, network-propagation]
raw: raw/papers/2025-06-16-fang-huo-li-wu-inattentive-network.pdf
---

# Fang, Huo, Li, and Wu, Inattentive Network (2025)

## Bibliographic

- Authors: Yue Fang, Zhen Huo, Minghao Li, and Jieran Wu
- Venue: working paper
- Date: 2025-06-16
- Raw file: `raw/papers/2025-06-16-fang-huo-li-wu-inattentive-network.pdf`

## Key claims

1. The [production network](../concepts/production-network.md) is given. Sector \(i\) produces \(Y_{i\iota t} = Z_{it} L_{i\iota t}^{\alpha_i} \prod_j X_{i\iota jt}^{a_{ij}}\). Firms do not choose suppliers. They choose signals about nominal marginal cost. Feeds [information friction](../topics/information-friction.md).
2. With elastic rational inattention, the firm tracks marginal cost at a constant marginal cost of mutual information. Price flexibility is \(\mu_i = 1 - \chi_i/(\theta_i\lambda_i\mathrm{V}(\mathrm{mc}_{it}))\). In partial equilibrium, attention to sector \(j\) rises with \(j\)'s prior variance and with \(a_{ij}^2\), and total capacity rises with \(\mathrm{V}(\mathrm{mc}_{it})\). Feeds [information friction](../topics/information-friction.md).
3. In general equilibrium, \(\mathbf{p}_t = (I - \mu A)^{-1}\mu(-I + \alpha\kappa)\mathbf{z}_t\), and \(\{\mu_i\}\) solve a fixed point. If one sector learns more, downstream marginal costs become more volatile and other sectors learn more. The response runs through \((I - A\mu)^{-1}A\). Feeds [network propagation](../topics/network-propagation.md) and [information friction](../topics/information-friction.md).
4. EDGAR browsing matches the partial-equilibrium predictions. A 10 percentage-point higher input share is associated with 44 percent more browsing of that supplier. A one-standard-deviation rise in the supplier's TFP volatility, equal to 0.12, is associated with 14.5 percent more browsing. Direct suppliers receive about 70 percent more attention than firms beyond distance 4, and distance-2 suppliers about 20 percent more. Total browsing rises with the variance of marginal-cost growth. A 50 percent increase in browsing over the prior 90 days is associated with a 2.2 percentage-point smaller earnings-per-share forecast error. The hazard of browsing is increasing. Feeds [information friction](../topics/information-friction.md).
5. [Monetary policy](../concepts/monetary-policy.md) is a wage rule \(w_t = \kappa z_t\), implemented as \(\sum_i \varphi_i p_{it} = 0\) with \(\varphi_i = \varphi_i^x + \varphi_i^e\). The first weight holds flexibility fixed and coincides with La'O and Tahbaz-Salehi. The second weight is expectation management: the wage rule changes marginal-cost volatility, firms change \(\mu\), and those changes feed back through the network. Optimal policy puts additional weight on sectors that start out rigid, which further reduces their incentive to learn. In the calibration the two weight vectors differ by 24.3 percent on average. Feeds [optimal monetary policy](../topics/optimal-monetary-policy.md).

## Figures and data

- EDGAR log files, with IP addresses recovered by the method in Chen, Cohen, Gurun, Lou, and Malloy (2020) and matched through ipinfo. Browsing is linked to FactSet customer–supplier pairs, Compustat, and a 71-sector input–output table.
- Table 3: log browsing on input share and supplier TFP or sales volatility.
- Figure 3: browsing coefficients by upstream network distance.
- Figure 4: browsing around the formation and termination of a trading relationship.
- Table 5: sectoral browsing on the variance of marginal-cost growth.
- Table 6: earnings-per-share and sales forecast errors on browsing over the prior 90 days.
- Figure 6: sectoral weights under elastic attention and under exogenous information. Figure 7: those weight gaps against initial flexibility, and the further dispersion of flexibility under the optimal rule.

## Pages updated

- [Production network](../concepts/production-network.md) (updated)
- [Monetary policy](../concepts/monetary-policy.md) (updated)
- [Information friction](../topics/information-friction.md) (created)
- [Optimal monetary policy](../topics/optimal-monetary-policy.md) (updated)
- [Network propagation](../topics/network-propagation.md) (updated)
