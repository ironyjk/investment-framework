---
name: rebalancing
version: "0.1.0"
description: "Rebalancing — the disciplined act of restoring portfolio weights that have drifted from their target allocation. Calendar vs. threshold (band) methods. Exploits mean reversion, controls risk, curbs behavioral biases. Trade-offs with taxes and fees."
---

# Rebalancing

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

## When to Use

- Any portfolio with an asset allocation (MPT, All Weather, Bogleheads — all in common)
- After a major rally or crash when weights have drifted significantly
- Life-stage changes (marriage, children, approaching retirement)
- Year-end tax optimization timing (loss harvesting)

## Practical Application

### Designing a Rebalancing Rule

```
1. Fix the target allocation
   Example: Equities 60 / Bonds 30 / Gold 10

2. Set bands (5/25 rule recommended — Swensen)
   - Absolute band 5%p or relative band 25%
   - Example: Equities 60 → 55~65% band

3. Decide frequency
   - At least annually + on band breach

4. Execution priority
   a) Sell-side rebalancing within tax-advantaged accounts (pension, ISA)
   b) Buy underweighted assets with new contributions
   c) Buy underweighted assets with dividends and distributions
   d) Sales in taxable accounts as a last resort

5. Calculate tax impact
   - If capital gains tax on sales > rebalancing benefit, reconsider
   - Check opportunities for Tax-Loss Harvesting
```

### Tax-Conscious Rebalancing Example

```
Situation: Equities 65% (target 60%), Bonds 25% (target 30%), Gold 10%

Bad approach: Sell 5% of equities → triggers capital gains tax
Good approach:
  - Direct next 3~6 months of new contributions entirely to bonds and gold
  - Rebalance equities→bonds within pension savings (연금저축) (no tax)
  - If there are loss-making positions at year-end, use swap trades to offset taxes
```

## Korean Context

### 1. Korean Tax Code and Rebalancing

- **Selling domestic equities**: No capital gains tax (except for large shareholders) → can rebalance freely
- **Selling foreign equities**: 22% capital gains tax (with a 2.5M KRW deduction) → sell-side rebalancing is expensive
- **Selling domestic ETFs**: 15.4% dividend income tax (on distributions + increase in holding-period tax basis) — as of 2026
- **Rebalancing within pension savings (연금저축)·IRP**: Tax deferred, fully tax-free rebalancing possible
- **Rebalancing within ISA**: Benefits from comprehensive taxation at maturity, tax-free during operation

### 2. Korean Tax-Efficient Rebalancing Order

1. Within **pension savings (연금저축)·IRP** first (no tax)
2. Within **ISA** next (tax-free during operation)
3. **Domestic equities and ETFs in taxable accounts** — free to sell (dividend/distribution taxes are separate)
4. **Foreign equities and foreign ETFs** — last, only within the annual 2.5M KRW deduction limit

### 3. Korea-Specific Situations

- **Dollar-denominated asset rebalancing**: FX fluctuations affect weights. Separate out and judge the FX contribution.
- **Real estate rebalancing is hard**: Lump-sum sales are impossible, liquidity is low → absorb adjustments on the financial-asset side
- **Failing to account for National Pension and retirement pensions**: These are also part of the asset allocation. Rebalancing must be viewed from a total portfolio perspective.

## Antipatterns & Overapplication

- **Rebalancing too often** — Monthly rebalancing only increases fees and taxes, with minimal benefit
- **Rebalancing too rarely** — Leaving a portfolio alone for 3~5 years causes large deviations from the intended risk level
- **Bands too narrow** — A 1%p band chases noise and only incurs costs
- **Ignoring taxes** — Large annual rebalancing in taxable accounts worsens after-tax returns
- **Emotional rebalancing** — "Equities have risen a lot, let's sell" with no rule = market timing
- **Giving up on rebalancing in a down market** — Missing the essential moment (buying at low prices)
- **Abusing tactical rebalancing** — "Given the macro outlook, I'll raise bond weights" = effectively market timing

## Limitations

1. **Return enhancement is small** — The main effect is risk control; do not expect return enhancement
2. **Loses out in long trend regimes** — In extended bull markets like the 1990s US equity dominance, rebalancing results in lost returns
3. **Tax costs can exceed the premium** — In high-tax brackets or with many foreign assets
4. **Optimal frequency and band cannot be theoretically determined** — Rules of thumb based on historical data
5. **Psychological difficulty** — Selling risen assets and buying fallen assets both run against emotion
6. **Cost-adjusted bias**: Some research shows the rebalancing premium disappears once taxes and fees are considered

## Used Together With

- `modern-portfolio-theory` / `all-weather` / `bogleheads` — The execution mechanism for all asset allocation strategies
- `dollar-cost-averaging` — DCA with new contributions is the best rebalancing method
- `korean-tax-optimization` — Designing tax-efficient rebalancing
- `behavioral-biases` — Rule-based trading instead of emotional trading

## When This Framework Is *Wrong*

- Single-asset concentrated investing → the concept of rebalancing itself is unnecessary
- Position sizing issues → `kelly-criterion`
- When the target allocation itself is wrong → go back to `modern-portfolio-theory` / `all-weather` to redesign
- Intent to time the market → that is not rebalancing

## Further Learning

- Swensen, D. (2005). *Unconventional Success*. — A rebalancing framework for individual investors.
- Vanguard (2010). "Best practices for portfolio rebalancing." — Empirical white paper.
- Jaconetti, C. et al. (Vanguard). "Sub-optimal is not always bad" — Tax-aware rebalancing.
- Korean application: Kim Sung-il, *Magical Money Management (마법의 돈 굴리기)* — rebalancing based on Korean ETFs.
