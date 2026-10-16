---
type: topic
title: "Information friction"
summary: "A limit on what agents know when they choose. Papers differ on the formalization, the real transmission, and the puzzles it explains."
created: 2026-10-16
updated: 2026-10-16
tags: [information-friction, production-network, monetary-policy]
sources: [wiki/sources/2022-05-01-lao-tahbaz-salehi-optimal-monetary-policy-production-networks.md, wiki/sources/2025-06-16-fang-huo-li-wu-inattentive-network.md]
---

# Information friction

Exogenous signals, sticky information, fixed information capacity, and elastic rational inattention are entries here, not separate concepts.

## How it is modelled

- La'O and Tahbaz-Salehi. Firms set nominal prices from private signals about productivity and do not observe the aggregate state. The information structure is exogenous: signals may depend on the productivity shocks and not on prices. Sticky information, in which a fraction of firms see the shocks and the rest price from the prior, is a special case. Price flexibility \(\phi_i\) is a parameter. Source: [Optimal Monetary Policy in Production Networks](../sources/2022-05-01-lao-tahbaz-salehi-optimal-monetary-policy-production-networks.md).
- Fang, Huo, Li, and Wu. Firms are rationally inattentive with elastic capacity. Under a quadratic approximation they track nominal marginal cost at a constant marginal cost \(\chi_i\) of mutual information. If \(\chi_i\) is low enough relative to the benefit, the firm buys one noisy signal of marginal cost. Price flexibility is chosen, \(\mu_i = 1 - \chi_i/(\theta_i\lambda_i\mathrm{V}(\mathrm{mc}_{it}))\). A fixed information capacity leaves total information unchanged when marginal-cost variance rises. Source: [Inattentive Network](../sources/2025-06-16-fang-huo-li-wu-inattentive-network.md).

## Interaction with the real economy

- In La'O and Tahbaz-Salehi, incomplete information makes nominal prices respond only insofar as the shocks are in the firm's signal. On a given [production network](../concepts/production-network.md), a stickier supplier lowers the upstream flexibility of its customers, so marginal costs and prices respond less to the nominal wage. [Monetary policy](../concepts/monetary-policy.md) cannot condition on a flexibility that firms choose, because flexibility is a parameter. Source: [Optimal Monetary Policy in Production Networks](../sources/2022-05-01-lao-tahbaz-salehi-optimal-monetary-policy-production-networks.md).
- In Fang, Huo, Li, and Wu, attention and prices are a fixed point. If sector \(j\) learns more, its price moves more, downstream marginal costs become more volatile, and other sectors acquire more information. The wage rule changes that volatility, so policy changes \(\mu\). Stabilizing sectors that are already rigid further reduces their incentive to learn. Source: [Inattentive Network](../sources/2025-06-16-fang-huo-li-wu-inattentive-network.md).

## Phenomena and puzzles explained

- La'O and Tahbaz-Salehi account for monetary nonneutrality that is stronger when any industry, including an upstream supplier, is stickier, and for an optimal price index that deviates from consumption shares. The information structure is an input to that result, calibrated from price-change frequencies. Source: [Optimal Monetary Policy in Production Networks](../sources/2022-05-01-lao-tahbaz-salehi-optimal-monetary-policy-production-networks.md).
- Fang, Huo, Li, and Wu account for EDGAR browsing. A 10 percentage-point higher input share is associated with 44 percent more browsing of that supplier, and a one-standard-deviation rise in the supplier's TFP volatility is associated with 14.5 percent more browsing. Attention falls with network distance. Total browsing rises with the variance of marginal-cost growth, which a fixed capacity does not predict. Greater browsing over the prior 90 days lines up with smaller earnings-per-share forecast errors. The hazard of browsing is increasing. A Calvo hazard is flat. The same model produces a positive association between sectoral shock volatility and the frequency of price changes. Source: [Inattentive Network](../sources/2025-06-16-fang-huo-li-wu-inattentive-network.md).
