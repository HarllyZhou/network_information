# Diagnostic Expectation Distortion Propagation

## Diagnostic Expectation in a Production Network: A TANK Model

This note sketches a tractable framework for studying inflation dynamics in a production network when firms differ in how they form expectations. In each sector, a share of firms forms rational expectations, while the remaining share forms diagnostic expectations in the sense of Bordalo, Gennaioli, and Shleifer (2018). Diagnostic firms overreact to recent forecast revisions. Because sectors are connected through input-output linkages, this overreaction changes not only the pricing decisions of diagnostic firms themselves but also the marginal costs faced by downstream firms. The key object is therefore not diagnosticity alone, or centrality alone, but the interaction between a sector's diagnostic share, its diagnosticity parameter, and its position in the production network.

Here "TANK" means two firm types, rational and diagnostic, rather than the usual two-household New Keynesian environment.

## Motivation

Behavioral evidence suggests that real-world decision makers do not always form expectations as full-information rational agents. Bordalo, Gennaioli, and Shleifer (2018) introduce diagnostic expectations into economics and finance as a forward-looking form of representativeness-based overreaction. When a state becomes more likely after new information arrives, diagnostic agents overweight outcomes associated with that state. For a variable that follows a persistent process, this generates extrapolative forecasts: good news leads agents to overstate future good outcomes, and bad news leads agents to overstate future bad outcomes.

Carvalho, Eusepi, Moench, and Preston (2021) study how subjective beliefs can explain the joint dynamics of inflation and inflation expectations. Their framework is useful for thinking about expectation formation in inflation data, but it abstracts from a channel that is central in multisector economies: input-output linkages. In a production network, the price set by one sector becomes an input cost for other sectors. Hence, if upstream firms set prices using diagnostic beliefs, the resulting price distortion propagates through realized input prices. Downstream firms can be fully rational and still inherit the upstream diagnostic distortion through their marginal costs.

The project is built around this gap. A sector's contribution to inflation and inflation expectations should depend on both its behavioral type composition and its network position. Highly diagnostic but peripheral sectors may have small aggregate effects. Highly central sectors with low diagnosticity may propagate shocks strongly but not distort beliefs much. The potentially important cases are sectors with high diagnosticity, high diagnostic-firm shares, and high upstream centrality.

## Research Questions

1. How do firms set prices in a networked economy with a mixture of rational and diagnostic firms?

2. How do a sector's diagnostic share $\phi_i$, diagnosticity parameter $\theta_i$, and network centrality $\kappa_i$ jointly shape aggregate inflation $\Pi_t$ and inflation expectations?

3. What are the real effects of diagnostic belief distortions when they propagate through input-output linkages?

## Model

### Sectors, Firms, and Beliefs

There are $N$ sectors in a closed economy. In each sector $i$, there is a unit mass of firms indexed by $f \in [0,1]$. A share $1-\phi_i$ of firms forms rational expectations, denoted by $\mathbb E$, and a share $\phi_i$ forms diagnostic expectations, denoted by $\mathbb D$. The parameter $\phi_i \in [0,1]$ measures the prevalence of diagnostic firms in sector $i$.

For a variable $W_t$ whose law of motion is understood by firms, diagnostic expectations are

$$
\mathbb D_t[W_{t+\tau}]
= \mathbb E_t[W_{t+\tau}]
+ \theta_i\left(
\mathbb E_t[W_{t+\tau}]
- \mathbb E_{t-1}[W_{t+\tau}]
\right),
$$

where $\theta_i \geq 0$ is the diagnosticity parameter in sector $i$. When $\theta_i=0$, diagnostic and rational expectations coincide. When $\theta_i>0$, firms extrapolate in the direction of the latest forecast revision.

### Technology

Each firm in sector $i$ produces using labor and intermediate inputs:

$$
Y_{if,t}
= e^{z_{it}}\zeta_i L_{if,t}^{\gamma_i}
\prod_{j=1}^N X_{if,j,t}^{\alpha_{ij}},
$$

with

$$
\gamma_i + \sum_{j=1}^N \alpha_{ij} = \psi < 1.
$$

Sectoral productivity is

$$
z_{it} = \bar z_i + \epsilon^z_{it},
$$

where

$$
\epsilon^z_{it}
= \rho^z\epsilon^z_{i,t-1} + \nu^z_{it},
\qquad
\nu^z_{it}\overset{\text{i.i.d.}}{\sim}\mathcal N(0,\sigma_\nu^2).
$$

### Timing

Price setting is subject to Calvo rigidity. Each period, a firm keeps its previous price with probability $\omega$ and resets its price with probability $1-\omega$, where $\omega\in(0,1)$.

1. Before current productivity $z_{it}$ is realized, a firm that resets chooses $P_{if,t}$ based on its expectation mode. Rational firms use $\mathbb E$ and diagnostic firms use $\mathbb D_i$. A firm that does not reset sets $P_{if,t}=P_{if,t-1}$. The pricing objective for a resetting firm is expected profit,

$$
\Gamma_{if,t}
= (1-\tau_i)P_{if,t}Y_{if,t}
- W_tL_{if,t}
- \sum_{j=1}^N P_{jt}X_{if,j,t},
$$

where $\tau_i$ is a sectoral tax or subsidy.

2. After $z_{it}$ is realized, firms choose labor and intermediate inputs to minimize costs subject to demand at the price in place for the period.

### Sectoral Aggregation

Each sector has a CES aggregator:

$$
Y_{it}
=
\left(
\int_0^1 Y_{if,t}^{(\xi-1)/\xi}\,df
\right)^{\xi/(\xi-1)},
\qquad \xi>1.
$$

The sectoral price $P_{it}$ is set to maximize $P_{it}Y_{it}-\int_0^1 P_{if,t}Y_{if,t}\,df$. This aggregator earns zero profit, as in La'O and Tahbaz-Salehi (2022).

### Household

The representative household maximizes

$$
\mathbb E_t\sum_{s=0}^{\infty}\beta^s U(C_{t+s},L_{t+s}),
\qquad
\beta\in(0,1),
$$

with period utility

$$
U(C,L)=\log C-\chi\frac{L^{1+\varphi}}{1+\varphi},
\qquad
\chi>0,\quad \varphi>0.
$$

Final consumption is Cobb-Douglas across sectoral goods:

$$
C_t=\prod_{i=1}^N\left(\frac{C_{it}}{\rho_i}\right)^{\rho_i},
\qquad
\sum_{i=1}^N \rho_i=1.
$$

The household budget constraint is

$$
P_tC_t
=
\sum_{i=1}^N P_{it}C_{it}
\leq
W_tL_t
+ \sum_{i=1}^N\int_0^1 \Gamma_{if,t}\,df
+ T_t,
$$

where tax revenues are rebated lump-sum:

$$
T_t=\sum_{i=1}^N\int_0^1 \tau_iP_{if,t}Y_{if,t}\,df.
$$

### Nominal Anchor

To define inflation, the model needs a nominal anchor. Use an exogenous nominal demand process:

$$
M_t=P_tC_t.
$$

The log of nominal demand is exogenous, with constant growth $\mu$ and an optional AR(1) shock. This anchor pins down the aggregate price level and the nominal wage, so aggregate inflation is well defined:

$$
\Pi_t = \frac{P_t}{P_{t-1}}.
$$

### Market Clearing

For every sector $i$,

$$
Y_{it}
=
C_{it}+\sum_{k=1}^N\int_0^1 X_{kf,i,t}\,df,
$$

where $X_{kf,i,t}$ is sector $i$'s good used by firms in sector $k$. Labor clears:

$$
L_t=\sum_{i=1}^N\int_0^1 L_{if,t}\,df.
$$

Together with household optimality, firm cost minimization, price setting, aggregation, the nominal-demand rule, and government budget balance, these conditions define equilibrium.

## Analytical Targets

These objects are to be derived.

1. How $P_{it}$ changes with $\phi_i$ and $\theta_i$.

2. Inflation $\Pi_t$ and the inflation expectation $\mathbb R_t[\Pi_{t+\tau}]$, where $\mathbb R_t$ is the conditional realized expectation at period $t$ of a variable at $t+\tau$.

3. A centrality measure $\kappa_i$ for each sector. Compare inflation and inflation expectations across sectors through the interaction $\kappa_i \times \theta_i \times \phi_i$. This product denotes interaction, not necessarily multiplication.

4. How Calvo persistence $\omega$ changes the persistence of these objects.

## Quantitative Analysis

Calibrate the model and compare real variables, inflation, and inflation expectations when a shock hits sectors with different centralities and diagnosticities. Vary $\omega$ to see how price persistence changes these responses.

## Open Issues and Next Steps

1. **Existence and uniqueness.** The equilibrium with decreasing returns, heterogeneous beliefs, and Calvo rigidity is still to be characterized.

2. **Measurement of $\phi_i$.** The diagnostic share is empirically difficult to observe.

3. **Policy.** Once the positive model is solved, ask whether monetary policy should put extra weight on sectors with high centrality and high diagnosticity, following La'O and Tahbaz-Salehi (2022).

## References

Bordalo, Pedro, Nicola Gennaioli, and Andrei Shleifer. 2018. "Diagnostic Expectations and Credit Cycles." *The Journal of Finance* 73 (1): 199-227. BibTeX key: `bordaloDiagnosticExpectationsCredit2018`.

Carvalho, Carlos, Stefano Eusepi, Emanuel Moench, and Bruce Preston. 2021. "Anchored Inflation Expectations." Working Paper. BibTeX key: `carvalhoAnchoredInflationExpectations2021`.

La'O, Jennifer, and Alireza Tahbaz-Salehi. 2022. "Optimal Monetary Policy in Production Networks." *Econometrica* 90 (3): 1295-1336. BibTeX key: `laoOptimalMonetaryPolicy2022`.
