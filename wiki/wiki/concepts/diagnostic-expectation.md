---
type: concept
title: "Diagnostic expectation"
summary: "A forecast that overweights outcomes recent news makes representative. One parameter governs the extra weight."
created: 2026-10-16
updated: 2026-10-16
tags: [diagnostic-expectation, beliefs]
sources: [wiki/sources/2018-02-01-bordalo-gennaioli-shleifer-diagnostic-expectations-credit-cycles.md, wiki/sources/2026-10-16-bordalo-et-al-real-credit-cycle.md]
---

# Diagnostic expectation

## Definition

A diagnostic expectation replaces the objective conditional density with one that overweights outcomes recent news has made representative. Equation (2) on page 1281 is

\[
f^{\theta}(X_{t+1}\mid X_t)
\propto
f(X_{t+1}\mid X_t)
\left[
\frac{f(X_{t+1}\mid X_t)}{f(X_{t+1}\mid \mathbb{E}_{t-J}(X_t))}
\right]^{\theta}.
\]

\(\theta \ge 0\), and \(\mathbb{E}_{t-J}(X_t)\) is the rational expectation of \(X_t\) given information at \(t-J\). The term in brackets is the likelihood ratio of the current conditional density to the density conditional on that older expectation. \(\theta = 0\) recovers the objective density. \(\theta > 0\) overweights futures that have become more likely given the recent news.

For a normal AR(1), the same rule has a mean representation. If \(\omega_t = b\omega_{t-1} + \varepsilon_t\),

\[\mathbb{E}_t^\theta(\omega_{t+1}) = \mathbb{E}_t(\omega_{t+1}) + \theta[\mathbb{E}_t(\omega_{t+1}) - \mathbb{E}_{t-1}(\omega_{t+1})].\]

The agent does not compute the two rational expectations and add them. Oversampling representative states implies that the news term receives weight \(1+\theta\).

## Who holds it, and about what

The formula is the same. The models differ in which agent uses it and which random variable it is applied to.

- Bordalo, Gennaioli, and Shleifer (2018). The firm and the household hold the same diagnostic expectation. The variable is next period's aggregate state \(\omega_{t+1}\), an AR(1). Both use it as the perceived probability that firm \(\rho\) produces and repays, namely that \(\omega_{t+1} \ge \rho\). In the firm's profit maximization that probability scales revenue and debt service, so it cancels from capital demand. Investment moves because the household sets the contractual rate from the same expectation. Investors' forecasts of future credit spreads are not a second diagnosed variable. They pass the diagnostic expectation of future \(\omega\) through the spread equation, and that forecast omits the reversal of the spread. Source: [Diagnostic Expectations and Credit Cycles](../sources/2018-02-01-bordalo-gennaioli-shleifer-diagnostic-expectations-credit-cycles.md).
- Bordalo, Gennaioli, Shleifer, and Terry (2026). The firm and the lender hold the diagnostic expectation, with the same \(\theta\). The variables are next period's firm-level productivity \(z'\) and aggregate productivity \(A'\). Given the paper's AR(1) processes, the means are \(\rho_z(\log z + \theta\varepsilon_z)\) and \(\rho_A(\log A + \theta\varepsilon_A)\). The firm uses these beliefs to choose investment, debt, and default. The lender uses them to price default. Source: [Real Credit Cycles](../sources/2026-10-16-bordalo-et-al-real-credit-cycle.md).

## Evidence

- In the 2018 model, \(\theta\) is a fixed parameter of beliefs about \(\omega\). It is disciplined by the predictability of Blue Chip forecasts of credit spreads, not by a firm's own earnings forecast. Source: [Diagnostic Expectations and Credit Cycles](../sources/2018-02-01-bordalo-gennaioli-shleifer-diagnostic-expectations-credit-cycles.md).
- Bordalo, Gennaioli, Shleifer, and Terry estimate \(\theta\) near 1 from firm-level profit forecasts, and assign that same value to firms and to lenders. Source: [Real Credit Cycles](../sources/2026-10-16-bordalo-et-al-real-credit-cycle.md).

## Used by

- [Credit cycle](../topics/credit-cycle.md), as the belief mechanism.
- [Financial friction](../topics/financial-friction.md). In the 2018 model it prices repayment of the aggregate-state threshold. In the 2026 model it enters the firm's default decision and the lender's debt price.

## Disagreements

None recorded.
