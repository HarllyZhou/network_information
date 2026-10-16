---
type: topic
title: "Network propagation"
summary: "How a shock or a policy move travels through input-output linkages, and what that does to prices and quantities."
created: 2026-10-16
updated: 2026-10-16
tags: [production-network, network-propagation, monetary-policy]
sources: [wiki/sources/2020-01-01-acemoglu-azar-endogenous-production-networks.md, wiki/sources/2022-05-01-lao-tahbaz-salehi-optimal-monetary-policy-production-networks.md, wiki/sources/2025-06-16-fang-huo-li-wu-inattentive-network.md]
---

# Network propagation

## Propagation mechanism

- Acemoglu and Azar. An industry's unit cost depends on the prices of the goods in its supplier set. A lower price in one industry lowers its customers' unit costs, and the Leontief inverse \(\mathcal{L}(S) = (I - \alpha(S))^{-1}\) cumulates the indirect effects. When the [production network](../concepts/production-network.md) is chosen, a lower price also raises the return to adopting that industry as a supplier, which cuts further prices. Source: [Endogenous Production Networks](../sources/2020-01-01-acemoglu-azar-endogenous-production-networks.md).
- La'O and Tahbaz-Salehi. The network is given. To a first-order approximation, firm \(k\) in industry \(i\) sets \(\log p_{ik} = \alpha_i \mathbb{E}_{ik}[\log w] - \mathbb{E}_{ik}[\log z_i] + \sum_j a_{ij}\mathbb{E}_{ik}[\log p_j]\). Upstream flexibility is \(\rho = (I - A\Phi)^{-1}\alpha\). A stickier supplier lowers the upstream flexibility of its customers, so their marginal costs respond less to the nominal wage. Source: [Optimal Monetary Policy in Production Networks](../sources/2022-05-01-lao-tahbaz-salehi-optimal-monetary-policy-production-networks.md).
- Fang, Huo, Li, and Wu. The network is given and price flexibility is chosen. Prices are \(\mathbf{p}_t = (I - \mu A)^{-1}\mu(-I + \alpha\kappa)\mathbf{z}_t\). If sector \(j\) acquires more information, the response of sector \(i\)'s flexibility is proportional to the \((i,j)\) element of \((I - A\mu)^{-1}A\), scaled by the covariance of the two marginal costs. Source: [Inattentive Network](../sources/2025-06-16-fang-huo-li-wu-inattentive-network.md).

## Effect of propagation

- Acemoglu and Azar. A better technology, or a lower distortion, weakly reduces every price. Under the technology–price single-crossing condition it also weakly expands every supplier set. In a 391-sector calibration, a 1 percent TFP increase in computer and electronic product manufacturing adds 288 edges and raises real GDP by 0.72 percent, against 0.04 percent when no new links are allowed. Source: [Endogenous Production Networks](../sources/2020-01-01-acemoglu-azar-endogenous-production-networks.md).
- La'O and Tahbaz-Salehi. The pass-through of nominal demand into consumption is \((1 - \rho_0) / (1 + (\gamma - 1 + 1/\eta)\rho_0)\), with \(\rho_0 = \beta'\Phi(I - A\Phi)^{-1}\alpha\). Stickiness anywhere lowers this pass-through directly and, through customers' marginal costs, indirectly. The pass-through of the wage into industry \(i\)'s price is \(\phi_i\rho_i\). Source: [Optimal Monetary Policy in Production Networks](../sources/2022-05-01-lao-tahbaz-salehi-optimal-monetary-policy-production-networks.md).
- Fang, Huo, Li, and Wu. Learning propagates downstream: a more informative sector raises the variance of its customers' marginal costs, and those customers then learn more. Under the optimal wage rule, sectors that begin more rigid become still more rigid. Source: [Inattentive Network](../sources/2025-06-16-fang-huo-li-wu-inattentive-network.md).

## Problems and mitigations

- In Acemoglu and Azar, the extensive-margin cascade requires the technology–price single-crossing condition. When the network is held fixed, a small productivity change does not jump GDP. Source: [Endogenous Production Networks](../sources/2020-01-01-acemoglu-azar-endogenous-production-networks.md).
- In La'O and Tahbaz-Salehi, the pass-through formulas are a first-order approximation on a Cobb–Douglas network, and price flexibility \(\phi_i\) is an exogenous information parameter. Source: [Optimal Monetary Policy in Production Networks](../sources/2022-05-01-lao-tahbaz-salehi-optimal-monetary-policy-production-networks.md).
- Fang, Huo, Li, and Wu make that flexibility a choice. Their pass-through of attention is still a derivative on a Cobb–Douglas network, and the supplier sets remain fixed. Source: [Inattentive Network](../sources/2025-06-16-fang-huo-li-wu-inattentive-network.md).
