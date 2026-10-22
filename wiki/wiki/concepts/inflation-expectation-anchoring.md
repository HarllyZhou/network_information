---
type: concept
title: "Inflation expectation anchoring"
summary: "Whether long-run inflation expectations move with short-run surprises. Anchored means they move little. Unanchored means they track those surprises."
created: 2026-10-20
updated: 2026-10-20
tags: [inflation-expectation-anchoring, information-friction, monetary-policy]
sources: [wiki/sources/2023-01-01-carvalho-eusepi-moench-preston-anchored-inflation-expectations.md]
---

# Inflation expectation anchoring

## Definition

Inflation expectation anchoring is the sensitivity of long-run inflation expectations to short-run inflation surprises. Expectations are anchored when a spell of surprise inflation moves the long-run expectation little. They are unanchored when that spell leads people to mark the long-run expectation up or down by a large amount.

In Carvalho, Eusepi, Moench, and Preston the two cases are two estimators of the inflation mean \(\bar\pi_t\). Firms update

\[\bar\pi_t = \bar\pi_{t-1} + k_t^{-1} f_{t-1},\]

where \(f_{t-1}\) is the previous one-step forecast error. While a distance statistic built from the history of those errors stays below a threshold, the gain \(k_t^{-1}\) declines with the sample size. That is the anchored case. When the statistic crosses the threshold, the gain jumps to a constant \(g > 0\). That is the unanchored case: long-run expectations stay sensitive to short-run surprises.

## Evidence

- Estimated on US CPI inflation and short-term professional forecasts, 1955:I–2015:IV, the constant gain has posterior mean 0.145 and the threshold has posterior mean 0.029. Firms switch to the constant gain once the perceived mean leaves a band of roughly 2 to 3 percent. The same estimates track survey measures of long-term expectations that were not used in the estimation, including the surge into the early 1980s and the stability through 2008. Source: [Anchored Inflation Expectations](../sources/2023-01-01-carvalho-eusepi-moench-preston-anchored-inflation-expectations.md).

## Used by

- [Information friction](../topics/information-friction.md), as one formalization of what firms do not know.
- [Optimal monetary policy](../topics/optimal-monetary-policy.md), because the weight on the output gap governs whether a drift in \(\bar\pi_t\) feeds back into inflation.

## Disagreements

None recorded.
