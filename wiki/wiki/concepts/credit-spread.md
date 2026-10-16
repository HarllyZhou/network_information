---
type: concept
title: "Credit spread"
summary: "The excess of a risky debt yield over the risk-free rate. The formula depends on how default is modelled."
created: 2026-10-16
updated: 2026-10-16
tags: [credit-spread, financial-friction]
sources: [wiki/sources/2018-02-01-bordalo-gennaioli-shleifer-diagnostic-expectations-credit-cycles.md, wiki/sources/2026-10-16-bordalo-et-al-real-credit-cycle.md]
---

# Credit spread

## Definition

The credit spread is the extra yield on a risky debt claim over the risk-free rate. Two formalizations are on file.

In Bordalo, Gennaioli, and Shleifer (2018) a firm of risk \(\rho\) repays with probability \(\mu(\rho, \omega)\). Households require an expected return \(\beta^{-1}\), so

\[S(\rho, \mathbb{E}_t^\theta) = \left(\frac{1}{\mu(\rho, \mathbb{E}_t^\theta(\omega_{t+1}))} - 1\right)\beta^{-1}.\]

In Bordalo, Gennaioli, Shleifer, and Terry (2026) the claim is one-period defaultable debt with price \(q\), and

\[S = \frac{1}{q} - R.\]

## Evidence

- In the 2018 model, greater optimism about the aggregate state raises perceived repayment \(\mu\) and compresses the spread. Riskier firms have higher spreads. Source: [Diagnostic Expectations and Credit Cycles](../sources/2018-02-01-bordalo-gennaioli-shleifer-diagnostic-expectations-credit-cycles.md).
- In the 2026 model, lenders who break even set \(q_\theta(s,k',b') = \frac{1}{R}\mathbb{E}^\theta[1 + d^f_\theta(s',k',b')(\ell(k',b') - 1) \mid s]\). The spread is high when diagnostic beliefs put more weight on default. Recovery \(\ell\) is a fraction \(\gamma\) of depreciated capital. Source: [Real Credit Cycles](../sources/2026-10-16-bordalo-et-al-real-credit-cycle.md).

## Used by

- [Financial friction](../topics/financial-friction.md), as the price through which the friction hits investment.
- [Credit cycle](../topics/credit-cycle.md), as the financial leg of the boom and the reversal.

## Disagreements

None recorded.
