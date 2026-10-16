---
type: concept
title: "Production network"
summary: "Which industries use which goods as inputs. Those sets may be fixed, or each industry may choose them."
created: 2026-10-16
updated: 2026-10-16
tags: [production-network, network-formation, network-propagation]
sources: [wiki/sources/2020-01-01-acemoglu-azar-endogenous-production-networks.md, wiki/sources/2022-05-01-lao-tahbaz-salehi-optimal-monetary-policy-production-networks.md, wiki/sources/2025-06-16-fang-huo-li-wu-inattentive-network.md]
---

# Production network

## Definition

A production network assigns to each industry the set of goods it uses as inputs, and the intensity with which each good is used. Each source on this page is either **chosen** or **given**. In a chosen network, firms pick the supplier sets. In a given network, the input–output shares are parameters of technology.

## Evidence

### Chosen

- Acemoglu and Azar. Industry \(i\) produces \(Y_i = F_i(S_i, A_i(S_i), L_i, X_i)\) and chooses the supplier set \(S_i\) to minimize unit cost. The wage is the numeraire. Equilibrium price is distorted unit cost, \(P_i^\ast = (1+\mu_i)K_i(S_i^\ast, A_i(S_i^\ast), P^\ast)\). For Hicks-neutral Cobb–Douglas technology, \(K_i = A_i(S_i)^{-1}\prod_{j\in S_i} P_j^{\alpha_{ij}}\) and \(p^\ast = -\mathcal{L}(S^\ast)(a(S^\ast) - m)\), with \(\mathcal{L}(S^\ast) = (I - \alpha(S^\ast))^{-1}\). An equilibrium exists, prices are unique, and the network is generically unique. Source: [Endogenous Production Networks](../sources/2020-01-01-acemoglu-azar-endogenous-production-networks.md).

### Given

- La'O and Tahbaz-Salehi. Firm \(k\) in industry \(i\) produces \(y_{ik} = z_i \zeta_i \ell_{ik}^{\alpha_i} \prod_j x_{ij,k}^{a_{ij}}\), with labor share \(\alpha_i\) and \(\alpha_i + \sum_j a_{ij} = 1\). The input–output matrix \(A = [a_{ij}]\) is calibrated to expenditure shares. The Leontief inverse is \(\mathcal{L} = (I - A)^{-1}\). Firms do not choose which goods to use. Those fixed shares govern how a supplier's price enters its customers' marginal cost, and they enter the weights of the optimal price index. Source: [Optimal Monetary Policy in Production Networks](../sources/2022-05-01-lao-tahbaz-salehi-optimal-monetary-policy-production-networks.md).
- Fang, Huo, Li, and Wu. The same Cobb–Douglas shares are parameters. Firms choose signals about marginal cost and do not choose suppliers. The authors treat the network as exogenous. Browsing rises before a customer–supplier relationship forms and falls after it ends, which the static given network does not explain. Source: [Inattentive Network](../sources/2025-06-16-fang-huo-li-wu-inattentive-network.md).

## Used by

- [Network formation](../topics/network-formation.md), only for sources filed as chosen.
- [Growth](../topics/growth.md), for the chosen network in Acemoglu and Azar, because new products expand the sets from which firms choose.
- [Network propagation](../topics/network-propagation.md), for how a change in one industry's cost or stickiness moves other industries' prices.
- [Optimal monetary policy](../topics/optimal-monetary-policy.md), because the given network changes the price index that policy stabilizes.
- [Information friction](../topics/information-friction.md), because attention and pricing errors travel along the given shares.

## Disagreements

None recorded. Acemoglu and Azar are the chosen case. La'O and Tahbaz-Salehi, and Fang, Huo, Li, and Wu, are given cases.
