# Rebalancing -- Theoretical Foundation

## One-Line Summary

**"Sell what rose the most, buy what fell the most."** The act of periodically returning a portfolio that has drifted from its target weights. The essence is not return enhancement but rather *risk maintenance, emotional control, and exploitation of mean reversion*. But it trades off against taxes and fees.

## Theoretical Origins

- **Harry Markowitz (1952)** — MPT. Deviations from target weights push the portfolio off the efficient frontier → return needed.
- **William Sharpe (1991)** — "The Arithmetic of Active Management". The mathematics of market equilibrium and rebalancing.
- **Robert Shiller** — Provided evidence of mean reversion. The theoretical basis for selling overvalued assets and buying undervalued ones.
- Vanguard, Swensen (Yale) — Emphasized the centrality of rebalancing in practice.

## Core Concepts

### 1. Why Rebalance

- **Risk control**: If equities rise and the weight shifts from 60%→80%, the portfolio exceeds its designed risk level
- Exploits **mean reversion**: Assets that have risen for a long time are more likely to fall, and assets that have fallen for a long time are more likely to rise (weakly)
- **Discipline**: Following *rules* instead of emotional buying and selling (→ `behavioral-biases`)
- **Triggers taxes and fees**: Sales incur capital gains tax and commissions (a downside)

### 2. Two Methods

#### A. Calendar Rebalancing
- Execute unconditionally on a fixed schedule: annually, semi-annually, quarterly, etc.
- Simple and easy to automate
- Downside: Executes even when weights have barely changed, or waits through rapid shifts if they fall outside the schedule

#### B. Threshold Rebalancing
- Execute only when weights deviate by ±X% from the target
- Example: Equities 60% ±5%p → no action within the 55~65% band
- Minimizes taxes and fees
- Downside: Requires continuous monitoring

#### C. Hybrid
- At least once a year + interim execution on band breach
- The most commonly used approach in practice

### 3. Rebalancing's Contribution to Returns

- Vanguard research: Long-term CAGR changes are generally **within ±0.5%p**
- The main benefit is **risk-adjusted return**: improvement in Sharpe Ratio
- The rebalancing premium is largest in combinations of *high-volatility assets + low-correlation assets*

### 4. Tax-Efficient Rebalancing

- **Buy underweighted assets with new cash** (adjust weights without selling)
- Use dividends and distributions to buy underweighted assets
- Prioritize sell-side rebalancing in tax-advantaged accounts (ISA, pension savings (연금저축))
- Minimize sales in taxable accounts

