# Epidemic Diagnosticity in Production Network and Unanchored Inflation Expectations

## Introduction

Economists have studied a lot on inflation expectation anchoring to improve monetary policy effectiveness, whereas the inflation expectations,empirically, are not anchored in many times, or take a long time to anchor after shocks. This project tries to understand the reason why inflation expectations are hard to anchor from the perspective of firms' belief and connections.

Empirical evidence has shown that firms are not rational by testing the predictaiblity of the forecast error. A simple waty to explain the failure of the full information rational expectation (FIRE) models is to assume that firms are subject to diagnostic expectations (DE), following Bordalo et al. (2026, AER). Generally speaking, with DE, fimrs will tend to overreact to shocks, beinging more instabilities into the economy and making inflation expectations harder to anchor.

On the other hand, DE itself is not enough to explain the persistence of unanchored inflation expetations, since, according to Flynn and Sastry (2024, working paper), firms' narratives, that is. loosely speaking, beliefs, can switch based on how well their beliefs and forecasts mathc their information. Therefore, it is necessary to evaluate how distorted the information firms are obtaining is. An important source of information is the firms' upstream and downstream firms, implying that production network and input-output linakges are important in inflation expectation anchoring. If an upstream firms is diagnostic, then its pricing will also incorporate its distorted view, thus affecting the downstram firms' pricing decision. As a result, the anchoring of inflation expectations requires much time since diagnostic firms need more time to ''cure'' itself from diagnosticity.

## Goals

This project has four goals. 
- Empirically, we try to use firm-level data to examine whether diagnosticity applies to firms' expectations. 
- Theoretically, we try to build a TANK model with DE and in the spirit of infectious disease models to understand how belief distortions are contagious and to characterize conditions where anchoring is possible. 
- Quantitatively, we try to calibrate a quantitative model and show how long it may take for inflation expectations to anchor with different levels of aggregate diagnosticity and how sectoral diagnosticity combined with its network position generates persistent anchoring. 
- As an application, we try to make policy implications on how to anchor the inflation expectations.

## Diagnostic Expectations

Bordalo et al. (2018, JoF) introduced DE into the economics and finance literature. It models an overreaction in future expectations to current news. For a random variable $X_t$, the distorted distribution function $f^\theta$ can be formulated as
$$ f^{\theta}(X_{t+1} | X_t) \propto f(X_{t+1} | X_t) \left[\frac{f(X_{t+1} | X_t)}{f(X_{t+1} | \mathbb{E}_{t-J} X_t)}\right]^\theta , $$
where $f$ is the true conditional distribution and $\theta \geq 0$ is the *diagnosticity* parameter. When $\theta = 0$, the expectation boils down to the rational expectation.

With conditional normal distribution of $X_{t+1}|X_t$, we can have the following formula:
$$ \mathbb{E}^\theta_t X_{t+1} = \mathbb{E}_t X_{t+1} + \theta (\mathbb{E}_t X_{t+1} - \mathbb{E}_{t-J} X_{t+1}). $$

## Model Assumptions

This is a TANK model in a closed economy with $N$ sectors interconnected with input-output (IO) linkages. Here, the TA in TANK refers to two types of firms instead of households. The model lays its foundation on La'O and Tahbaz-Salehi (2022, Econometrica)。 L'Huiller and Singh (2024, REStud) provides solution methods for DENK models.

### Production Firms
Each sector $i$ has a unit mass of production firms $k \in [0,1]$. Assume that there are two types of firms in each sector: rational firms with $\theta = 0$ and diagnostic firms with diagnosticity $\theta_i > 0$. For the benchmark, we assume that $\theta_i = \theta$ for all $i$'s. Denote $\delta_i \in [0,1]$ as the proportion of diagnostic firms in sector $i$. 

Assume Calvo-type price stickiness such that there is a probability $\omega \in (0,1)$ that a firm cannot change its price. 

Firms are producing differentiated goods using a CES aggregator of intermediate inputs from sector $j$, $x_{ik,j}$ with a decreasing return to scale (DRTS) production technology
$$ y_{ik, t} = \zeta_i \left(\sum_{j=1}^N \alpha_{i,j} x_{ik, j, t}^{\frac{\xi_i}{\xi_i-1}}\right)^{\psi \frac{\xi_i-1}{\xi_i}}, $$
where $\alpha_{i,j} \in (0,1)$'s are the share parameters, $\xi_i$ captures substitutability, $\psi \in (0,1)$ captures the DRTS, and $\zeta_i$ is a normalizing factor to be defined when deriving the marginal cost.

Firms choose the price by maximizing the profit:
$$
\max_{p_{ik,t}}\quad \mathbb{E}^{\theta_k}_t \sum_{s=0}^{+\infty} (\Lambda_{0,s} \omega)^s \left(p_{ik,t} y_{ik, t+s} - \sum_{j=1}^N p_{j,t+s} x_{ik,j,t+s}\right), $$
where $\theta_k  = \theta$ if firm $k$ is diagnostic and $0$ otherwise. 

### Aggregation Firms
Competitive aggregators aggregate the differentiated goods produced by production firms under a CES production technology:
$$
y_{i,t} = \left(\int^1_0 y_{ik,t}^{\frac{\chi_i - 1}{\chi_i}} dk\right)^{\frac{\chi_i}{\chi_i-1}}.
$$
Their competitiveness implies that the sector $i$ good is priced at such that the aggregators earn zero profit:
$$
V^A_{i,t} = p_{i,t} y_{i,t} - \int^1_0 p_{ik,t} y_{ik,t} dk = 0.
$$

### Household
Households are standard ones with CRRA utility derived from a consumption aggregator $C_t = \prod_{i=1}^N \left(\frac{c_{i,t}}{\phi_i}\right)^{\phi_i}$ and maximize their lifetime utility with discount factor $\beta \in (0,1)$:
$$ \max_{C_t}\quad \mathbb{E}_0 \sum_{s=0}^{+\infty} \beta^s \frac{{C_t}^{1-\gamma}}{1-\gamma} $$
subject to the budget constraint
$$ P_t C_t = \sum_{i=1}^N p_{i,t} c_{i,t} \leq V_t + T_t, $$
where $V_t$ is the total profit of all firms in this economy and $T_t$ is a lump-sum transfer from the government. 

### Monetary Authority
We follow La'O and Tahbaz-Salehi (2022, Econometrica) and impose the cash-in-advance constraint on the household's total expenditure:
$$
P_t C_t = M_t,
$$
where $M_T$ that can be interpreted as either monet supply or nominal aggregate demand is set directly by the monetary authority.