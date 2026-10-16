---
type: topic
title: "Credit cycle"
summary: "The expansion and reversal of credit spreads, debt, and investment, and how papers model and test that pattern."
created: 2026-10-16
updated: 2026-10-16
tags: [credit-cycle, diagnostic-expectation]
sources: [wiki/sources/2018-02-01-bordalo-gennaioli-shleifer-diagnostic-expectations-credit-cycles.md, wiki/sources/2026-10-16-bordalo-et-al-real-credit-cycle.md]
---

# Credit cycle

## Methodology

- Bordalo, Gennaioli, and Shleifer (2018) use a production economy in which the firm and the household share a [diagnostic expectation](../concepts/diagnostic-expectation.md) of the aggregate state \(\omega_{t+1}\). A firm repays when that state clears its risk threshold. The household prices the debt. The comparison case is \(\theta = 0\). Motivating evidence is Blue Chip forecasts of Baa spreads. Source: [Diagnostic Expectations and Credit Cycles](../sources/2018-02-01-bordalo-gennaioli-shleifer-diagnostic-expectations-credit-cycles.md).
- Bordalo, Gennaioli, Shleifer, and Terry (2026) link IBES manager guidance to Compustat and to FISD–TRACE bond data, then estimate a heterogeneous-firm model by simulated method of moments. The firm and the lender both hold a diagnostic expectation, about productivity. The friction is one-period defaultable debt with an optimal default choice. The comparison model sets diagnosticity to zero. Source: [Real Credit Cycles](../sources/2026-10-16-bordalo-et-al-real-credit-cycle.md).

## Results

- Bordalo, Gennaioli, and Shleifer (2018). Good news compresses the [credit spread](../concepts/credit-spread.md) and raises investment. The household's overreaction then reverses, so the spread is an ARMA(1,1) and boom-bust cycles appear. Under rational expectations the spread is an AR(1) and does not reverse on its own. Forecast errors of credit spreads are predictable. When optimism is high, riskier firms issue more. Source: [Diagnostic Expectations and Credit Cycles](../sources/2018-02-01-bordalo-gennaioli-shleifer-diagnostic-expectations-credit-cycles.md).
- Fragility after good times. In Bordalo, Gennaioli, Shleifer, and Terry (2026), good news raises investment and debt and compresses spreads, because firms and lenders both overreact. When the news ages, spreads rise, investment falls, and defaults rise, even if the fundamental shock is moderate. Diagnosticity near 1 matches the 2007–2009 spread spike. Rational expectations do not. Source: [Real Credit Cycles](../sources/2026-10-16-bordalo-et-al-real-credit-cycle.md).

## Problems and mitigations

- In the 2018 model, default is a threshold on the aggregate state rather than a value comparison, the diagnosed variable is that aggregate state rather than firm productivity, and \(\theta\) is not estimated from a firm's earnings forecast. Bordalo, Gennaioli, Shleifer, and Terry (2026) replace the threshold with the firm's default decision, apply the diagnostic expectation to firm-level and aggregate productivity, and estimate \(\theta\) from profit forecasts. Source: [Diagnostic Expectations and Credit Cycles](../sources/2018-02-01-bordalo-gennaioli-shleifer-diagnostic-expectations-credit-cycles.md).
- The 2026 baseline holds the wage and the risk-free rate fixed, the recovery rate is an exogenous fraction of depreciated capital, and debt lasts one period. The paper endogenizes the wage in general equilibrium and the reversal remains. No later source in the wiki yet addresses one-period debt or the absence of an intermediary. Source: [Real Credit Cycles](../sources/2026-10-16-bordalo-et-al-real-credit-cycle.md).
