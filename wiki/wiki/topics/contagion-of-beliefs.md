---
type: topic
title: "Contagion of beliefs"
summary: "How a belief becomes more common because others already hold it, and what that spread does to output."
created: 2026-10-22
updated: 2026-10-22
tags: [contagion-of-beliefs, narrative, information-friction]
sources: [wiki/sources/2024-06-01-flynn-sastry-macroeconomics-of-narratives.md]
---

# Contagion of beliefs

Contagion, association, and stubbornness are entries here, not separate concepts.

## How beliefs spread

- Flynn and Sastry. The probability that a firm holds the optimistic [narrative](../concepts/narrative.md) next period rises with its own current narrative, with the share of optimists \(Q\), and with current output. In the linear rule those loadings are stubbornness \(u\), contagiousness \(s\), and associativeness \(r\): \(P_O = [u/2 + r\log Y + sQ + \varepsilon]_0^1\) and \(P_P = [-u/2 + r\log Y + sQ + \varepsilon]_0^1\). Contagion is the loading on \(Q\). Association is the loading on output. In the 10-K panel the estimates are \(u=0.21\), \(s=0.29\), and \(r=0.80\). Within an industry, and with time fixed effects, the leave-one-out optimistic share has loading 0.28 and industry output growth has loading 0.06. Source: [The Macroeconomics of Narratives](../sources/2024-06-01-flynn-sastry-macroeconomics-of-narratives.md).

## Effect on the economy

- In the unique quasi-loglinear equilibrium, log output is linear in productivity and separable in the optimistic share. The gap in log output between unanimous optimism and unanimous pessimism is \(\alpha\delta^{OP}/(1-\omega)\). Optimistic firms hire 3.6 percentage points more. The calibrated demand multiplier is 1.96, so the general-equilibrium output effect is larger than the hiring effect of one firm. Source: [The Macroeconomics of Narratives](../sources/2024-06-01-flynn-sastry-macroeconomics-of-narratives.md).
- On the historical path of measured optimism, the optimistic component accounts for 32 percent of the output loss from 2000 to 2002 and 18 percent from 2007 to 2009. In model simulations, optimism accounts for 19 percent of output variance, 33 percent of one-year autocovariance, and 79 percent of two-year autocovariance. Productivity shocks in the same calibration have persistence 0.086. Shutting down stubbornness, contagion, and association leaves 4 percent of output variance and none of the autocovariance. Source: [The Macroeconomics of Narratives](../sources/2024-06-01-flynn-sastry-macroeconomics-of-narratives.md).
- Unanimous optimism and unanimous pessimism are both steady states when the output gap between them is large relative to the output levels that sustain each narrative on its own. For the linear rule the statistic is \(\hat M = \hat u + \hat s + \hat r\,\alpha\hat\delta^{OP}/(1-\omega) - 1\). Aggregate optimism has \(\hat M = -0.44\), so it fluctuates around an interior steady state. Many granular narratives have a statistic at or above zero. Optimism formed as a weighted sum of those narratives still explains 16 percent of output variance. Source: [The Macroeconomics of Narratives](../sources/2024-06-01-flynn-sastry-macroeconomics-of-narratives.md).

## Problems and mitigations

- The baseline contagion regression uses lagged aggregate optimism, so it is not the contemporaneous reflection problem. Common shocks can still move both aggregate optimism and later firm language. Adding two leads and two lags of GDP growth leaves the aggregate contagion coefficient in the same range. A granular instrument built from idiosyncratic optimism at large firms, and spillovers from CEO exits coded as death, illness, or retirement, give contagion coefficients of the same sign. Source: [The Macroeconomics of Narratives](../sources/2024-06-01-flynn-sastry-macroeconomics-of-narratives.md).
- The demand multiplier is set from an external calibration: constant returns, no income effect on labor supply, an inverse Frisch elasticity of 0.4, and a demand elasticity of 2.6. The contribution of optimism rises with the multiplier. A multiplier of 1.33, taken from other estimates of demand multipliers, is one of the alternatives the paper reports. Source: [The Macroeconomics of Narratives](../sources/2024-06-01-flynn-sastry-macroeconomics-of-narratives.md).
- The updating probabilities are a linear probability model, trimmed to the unit interval. At the estimates, those probabilities stay inside the interval when output stays within 30 percent of steady state. The model is a real business-cycle model with monopolistic competition. Household expectations are left unrestricted. Source: [The Macroeconomics of Narratives](../sources/2024-06-01-flynn-sastry-macroeconomics-of-narratives.md).
