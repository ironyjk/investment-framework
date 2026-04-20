# Modern Portfolio Theory (MPT) -- Theoretical Foundation

## One-Line Summary

Not "how much do you earn" but **"how much can you reduce volatility while achieving the same return"**. The core of MPT is exploiting **correlations** between assets to obtain a *free lunch* (diversification benefit).

## Theoretical Origins

- **Harry Markowitz (1952)** — "Portfolio Selection", *Journal of Finance*. 1990 Nobel Prize in Economics.
- **William Sharpe (1964)** — CAPM, Sharpe Ratio.
- **James Tobin (1958)** — Separation Theorem, introduction of the risk-free asset.
- The **starting point** of modern portfolio theory. All-Weather, Risk Parity, and Factor Investing are all variations or extensions of MPT.

## Core Concepts

### 1. Expected Return vs. Volatility
- Summarize each asset with two numbers: return (E[R]) and volatility (σ)
- **Risk = volatility (standard deviation)** as a simplification — MPT's biggest simplification and limitation
- **Normal distribution · iid assumption**: the premise that returns follow a normal distribution and are independently and identically distributed across periods. Actual financial time series exhibit (1) autocorrelation and volatility clustering, (2) negative skew, (3) excess kurtosis (fat tails). Events of 6σ+ like 2008, 2020, and 2022 are observed once every few decades.

### 2. Correlation (ρ) Is the Magic
- If two asset returns move in perfect sync (ρ=1), there is no diversification benefit
- **If ρ < 1, portfolio volatility is lower than the weighted average** — mathematically proven
- Combinations of negatively correlated (ρ<0) assets are the most powerful

### 3. Efficient Frontier
- The curve of portfolios that satisfy "maximum return for the same risk" or "minimum risk for the same return"
- *Above* this curve is impossible, *below* it is inefficient
- Real-world asset allocation is the problem of choosing a single point on this curve

### 4. Sharpe Ratio
$$\text{Sharpe} = \frac{E[R] - R_f}{\sigma}$$
- Excess return per unit of risk. The standard metric for portfolio evaluation
- **The normal distribution trap**: actual returns have heavy left tails (negative skew, excess kurtosis). Even with the same Sharpe, hedge funds and option-selling strategies have tail losses that are not reflected in Sharpe → overvaluation.
- Alternative metrics: **Sortino Ratio** (downside volatility only), **Calmar Ratio** (MDD-based), **Omega Ratio** (based on the full distribution). MPT's Sharpe is reliable *only when the distribution is close to normal*.

### 5. Risk-Free Asset + Risky Asset Combination (Capital Market Line)
- Mixing a risk-free asset (cash or government bonds) with the tangent portfolio beats the Frontier
- Scale the risk level with leverage or deleverage

## Modern MPT Advances (Reference)

Modern techniques that address the limitations of Markowitz's original work:

- **Black-Litterman Model (1990)**: combines CAPM equilibrium returns as a prior with investor views as a posterior. Mitigates input sensitivity and extreme-weight issues.
- **Resampled Efficient Frontier (Michaud 1998)**: averages multiple frontiers via Monte Carlo. Stable weights.
- **Risk Parity** (→ `all-weather`): removes dependence on expected return estimates.
- **Hierarchical Risk Parity (López de Prado 2016)**: hierarchizes the correlation structure via machine-learning clustering. Avoids the matrix-inversion instability of traditional MPT.
- **Robust Optimization**: embeds input uncertainty as explicit constraints.

Implication for individual investors: do not accept the output of Efficient Frontier software as *optimal*. Modern researchers don't use the original MPT as-is either.

