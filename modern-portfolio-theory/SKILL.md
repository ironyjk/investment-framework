---
name: modern-portfolio-theory
version: "0.1.0"
description: "Modern Portfolio Theory (Markowitz 1952) — optimize overall portfolio risk and return. Efficient Frontier, correlation-based diversification, Sharpe ratio. The theoretical starting point for asset allocation decisions."
---

# Modern Portfolio Theory (MPT)

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

## When to Use

- "How do I set my stock:bond:gold allocation?" — asset class allocation decisions
- Counter-argument to "Is it OK to put it all in one asset?"
- Evaluating the Sharpe ratio of an existing portfolio
- Checking *whether diversification benefits arise from correlation* when adding a new asset
- The theoretical foundation of an institutional investor's IPS (Investment Policy Statement)

## Practical Application

```
1. Define asset classes (5-10)
   e.g., Korean equities, developed-market equities, emerging-market equities, Korean bonds, foreign bonds, gold, REITs, cash
2. Estimate expected return, volatility, and correlation for each asset
   - 10-20 years of historical data is the starting point (but not a prediction of the future)
3. Simulate the Efficient Frontier
   - Excel, Python (pandas, scipy.optimize), online tools (Portfolio Visualizer)
4. Select a point matching your risk tolerance
   - Under 10% volatility? 15%? 20%?
5. Check actual returns and volatility on a monthly/quarterly basis; if the gap from theory is large, revisit the assumptions
```

## Korean Context

### Caveats When Korean Investors Apply MPT
- **KOSPI and KOSDAQ have high correlation with US and European equities** (globalization). The diversification effect of pure "domestic stocks" is limited.
- **KRW asset bias (home bias)** — 80%+ of Korean investors' assets are in KRW. From a currency-hedge perspective, foreign assets already contribute to *diversification*.
- **Real estate weight is the true driver of the portfolio**: the average Korean household has 70%+ of its assets in real estate. Excluding it from MPT calculations creates a gap with reality.
- **Bond accessibility**: US Treasury ETFs (TLT, IEF) carry currency risk for KRW investors. Distinguish them from KRW bond ETFs such as KODEX Korea Treasury Bond.
- **Financial investment tax (금투세) and dividend tax**: Sharpe should be recalculated on an after-tax return basis to reflect Korean reality.

### General Frames for Korean Investors (Not a Recommendation, Just Examples)
- Aggressive (20s-30s): 60 foreign equities / 20 domestic equities / 10 gold·REITs / 10 cash·bonds
- Balanced (40s): 40 foreign equities / 15 domestic equities / 25 bonds / 10 gold·alternatives / 10 cash
- Conservative (50s+): 25 foreign equities / 10 domestic equities / 45 bonds / 10 gold / 10 cash
- The above are *examples* and must be recalculated in the context of overall assets including real estate, retirement benefits, and National Pension.

## Antipatterns & Overapplication

- **Predicting the future directly from historical data** — just because the 10-year Sharpe was 1.2 doesn't mean it will be 1.2 going forward
- **Trusting Efficient Frontier accuracy** — a 5% input error → a 30% output difference (extreme model sensitivity)
- **Assuming correlations are static** — during a crisis all correlations converge to 1 (the diversification effect disappears)
- **The simplification volatility = risk** — upside volatility is also counted as "risk". Tail risk is not reflected.
- **Applying it at the individual stock level** — MPT is useful for asset class allocation, but unsuitable for picking 10 stocks
- **Recalculation compulsion** — if you re-run the Frontier and rebalance every month, transaction costs and taxes offset the gains

## Limitations

1. **Normal distribution assumption** — actual returns have fat tails. Underestimates extreme events.
2. **Past = future assumption** — vulnerable to regime changes (interest rates, inflation, geopolitics).
3. **Volatility = risk assumption** — criticized most strongly by Taleb. True risk is permanent loss.
4. **Ignores transaction costs and taxes** — absent in theory, but decisive in practice.
5. **Assumption that investor utility is mean-variance utility** — actual humans have loss aversion and regret aversion biases (→ `behavioral-biases`).
6. **Input sensitivity** — slight errors in expected return inputs lead to drastically different optimal solutions (Michaud's "error maximization" critique).

## Modern MPT Advances (Reference)

Modern techniques that address the limitations of Markowitz's original work:

- **Black-Litterman Model (1990)**: combines CAPM equilibrium returns as a prior with investor views as a posterior. Mitigates input sensitivity and extreme-weight issues.
- **Resampled Efficient Frontier (Michaud 1998)**: averages multiple frontiers via Monte Carlo. Stable weights.
- **Risk Parity** (→ `all-weather`): removes dependence on expected return estimates.
- **Hierarchical Risk Parity (López de Prado 2016)**: hierarchizes the correlation structure via machine-learning clustering. Avoids the matrix-inversion instability of traditional MPT.
- **Robust Optimization**: embeds input uncertainty as explicit constraints.

Implication for individual investors: do not accept the output of Efficient Frontier software as *optimal*. Modern researchers don't use the original MPT as-is either.

## What to Use With This Framework

- `all-weather` — an application reorganizing MPT's correlation philosophy by economic regime
- `bogleheads` — a practical simplification of MPT into minimum-cost, 3-fund form
- `factor-investing` — an extension decomposing MPT's expected-return explanation into factors
- `rebalancing` — the execution mechanism that maintains the weights MPT specifies

## When This Framework Is *Wrong*

- Preparing for tail risk and black swans → `barbell-strategy`
- Behavioral and psychological issues → `behavioral-biases`
- Finding undervalued individual stocks → `value-investing`
- Korean after-tax returns → `korean-tax-optimization`
- Staggered-buy timing → `dollar-cost-averaging`

## Further Learning

- Markowitz, H. (1952). "Portfolio Selection." *Journal of Finance*.
- Bernstein, W. *The Intelligent Asset Allocator* (2000). — A masterpiece of MPT popularization.
- Swensen, D. *Pioneering Portfolio Management* (2000). — The Yale Endowment application.
- Online: Portfolio Visualizer (portfoliovisualizer.com) — free Efficient Frontier simulation.
- Criticism: Taleb *The Black Swan* — the representative critique of MPT's limitations.
