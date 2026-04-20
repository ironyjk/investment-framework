---
name: kelly-criterion
version: "0.2.0"
description: "Kelly Criterion (John L. Kelly Jr., 1956) — the betting-size formula that maximizes long-run asset growth rate. Fractional Kelly (1/2, 1/4) dampens volatility. Manages probability of ruin. The mathematical standard for position sizing."
---

# Kelly Criterion

> Background and theory: Read references/foundation.md



## When to Use It

- **Sizing individual bets** — How much to allocate to a single position
- **Leverage limits** — Determining maximum leverage ratio
- **Options/derivatives position sizing**
- **Per-trade size for automated trading bots**
- **Setting upper bounds for concentrated-investment strategies**
- Systematic trading strategies (when win rate and payoff ratio are estimable)

## Practical Application

### Example 1: Based on Stock Expected Return/Volatility

```
Assumptions:
- Stock portfolio expected return μ = 8%
- Risk-free rate r = 3%
- Volatility σ = 18%

Full Kelly:
f* = (0.08 - 0.03) / 0.18² = 0.05 / 0.0324 ≈ 154%

→ Full Kelly calls for 1.54x leverage (!!)
→ Absurdly aggressive for most investors
→ ¼ Kelly: 38% (i.e., 38% in stocks, no leverage)
```

### Example 2: Binary Bet (Speculative)

```
Assumption: 70% chance of doubling, 30% chance of total loss
b = 1, p = 0.7, q = 0.3

f* = (1 × 0.7 - 0.3) / 1 = 40%

→ Full Kelly: Bet 40% of assets
→ ½ Kelly: 20%
→ ¼ Kelly: 10%
```

### Example 3: Automated Trading Bot (kisdev context, SOXL 3x leverage)

```
Assumptions: Automated trading bot for SOXL (semiconductor 3x leveraged ETF)
- Backtest: monthly expected return 3%, monthly volatility 10% (annual σ≈35%)
- Avg 20 trades per month, 55% win rate, avg payoff ratio 1.3

Caution: SOXL is already a 3x leveraged asset — when computing Kelly, σ must
be treated as 3x the underlying (SOX), and daily rebalancing decay (volatility drag)
means long-term expected return is not 3x the underlying.

Annualized Kelly estimate:
μ(annual) ≈ 3% × 12 = 36% (risk of backtest overconfidence)
σ(annual) ≈ 10% × √12 ≈ 35%
r ≈ 3%
Full Kelly = (0.36 - 0.03) / 0.35² ≈ 2.7x leverage

→ Since SOXL is already 3x, Full Kelly assumes no additional leverage
→ Accounting for backtest overfitting: halve μ (18%), scale σ by 1.5x (50%)
   conservatively → f* = (0.18-0.03)/0.25 = 60%
→ ¼ Kelly = 15% → Allocate only 15% of total assets to the SOXL bot
→ If kisdev's $8K is within ~10% of total assets ($80K+ assumed), it's consistent
   with both Barbell and Kelly
```

**Checklist for deciding to increase principal**:
1. Is the live trading Sharpe ratio at least 60% of the backtest's (reflecting typical decay)?
2. Over 3+ years of live trading, is the maximum drawdown within the allowed range (e.g., 5% of total assets)?
3. User context: 3 children · funds for switching into Ulsan housing · KRW 180M labor income — can the life plan hold even if this money goes to zero (the condition for the aggressive leg of Barbell)?
4. When increasing, add only **¼** of the Kelly-calculated value (e.g., $8K → $10K incrementally)

## Korean Context

### 1. Why Kelly Is Risky for Korean Investors

- **Difficulty in parameter estimation**: μ and σ are not known precisely. Historical data routinely leads to overestimation of Full Kelly for the future.
- **Temptation toward single-asset over-concentration**: Applying Full Kelly can push 40–80% of capital into a single name. Conflicts with diversification principles.
- **Leverage culture**: Korea's margin trading and 미수 (missu, unsettled credit) culture distorts Kelly into an accelerator of ruin
- **Taxes not reflected**: Must be recomputed on an after-tax expected-return basis

### 2. Kelly Usage Guide for Korean Investors

- **Never use Full Kelly** — Once estimation error is considered, actual Kelly is less than half the computed value
- **Start with ¼ Kelly** + be even more conservative for individual names (⅛ Kelly or less)
- **Restrict leverage use to under ½ Kelly**
- **Automated trading bots**: Use only 30–50% of the computed value, accounting for backtest overfitting

### 3. Link to the kisdev (SOXL Bot) Case

- Current structure: KRW 1M monthly contributions + $8K managed
- Do not use the Full Kelly computation as your actual position
- Assume a conservative μ of about ½ of the backtest's expected return
- Assume a conservative σ of 1.5x the actual backtest's value
- User's note: "direction of principal/parameter optimization" — Kelly can serve as the ceiling reference for scaling the principal

## Antipatterns & Over-Application

- **Using Full Kelly** — No consideration of estimation error, accelerates ruin
- **Overestimating win probability** — p is really 0.55 but you assume 0.70 for the Kelly calculation
- **Assuming independence when bets aren't independent** — When multiple names share the same factor exposure, Kelly's diversification meaning diminishes
- **Going all-in on one name per Full Kelly without leverage** — 80% of assets in a single name
- **Doubling down after losses to recover** — Increasing bet size to recover losses is the opposite direction of Kelly
- **Mistaking Kelly for return maximization** — Kelly maximizes geometric mean. Different from arithmetic mean and Sharpe.
- **Overconfidence in short-run win rate** — Computing win rate from 10 trades → all coincidence. Need at least hundreds.

## Limitations

1. **Impossibility of parameter estimation** — Actual μ·σ·p·b are future values and therefore unknowable. Kelly is *optimal only for theoretical values*.
2. **Extreme sensitivity to estimation error** — A 10% input error → 30%+ error in Kelly
3. **Large short-term drawdowns** — A 50% drawdown is common under Full Kelly
4. **Psychologically unsustainable** — Even "mathematically optimal," you may not actually endure it
5. **Violation of continuous-time / infinite-divisibility assumption** — If the continuous-time assumption is violated, ruin probability emerges
6. **Independence assumption** — Financial markets have autocorrelation and regime changes, violating Kelly's assumptions
7. **Taxes and transaction costs not reflected** — Actual returns differ substantially
8. **Special nature of log utility (Samuelson's critique)**: Kelly is optimal for a log-utility investor, not universally optimal. For an average investor with CRRA coefficient γ=2~4, 1/γ Kelly (=1/2~1/4 Kelly) maximizes utility.
9. **Power-law nature of cumulative distributions** — Actual financial market returns are fat-tailed. The Kelly formula uses normal/log-normal assumptions and underestimates tail losses.

## Frameworks to Use Alongside

- `barbell-strategy` — Determines sizing for the aggressive leg of the Barbell
- `value-investing` — Upper bound for concentrated single-name investing
- `behavioral-biases` — Mathematical control over overconfidence and gambling biases
- `modern-portfolio-theory` — MPT is mean-variance; Kelly is geometric-mean. Complementary.

## When This Framework Is *Wrong*

- Diversified-investing based (Bogleheads) → Kelly is mostly unnecessary
- Long-term asset-allocation problems → `modern-portfolio-theory` / `all-weather`
- Psychological issues → `behavioral-biases`
- Buy-timing → `dollar-cost-averaging`

## Further Reading

- Kelly, J. L. (1956). "A New Interpretation of Information Rate." *Bell System Technical Journal*.
- Thorp, E. (1969). "Optimal Gambling Systems for Favorable Games."
- Poundstone, W. (2005). *Fortune's Formula*. — Popular book.
- MacLean, Thorp, Ziemba (2011). *The Kelly Capital Growth Investment Criterion*. — Academic compilation.
- Hsu (2008). "Kelly and Half-Kelly for Common Investors" — Rationale for fractional Kelly.
- Critique: Paul Samuelson's Kelly-critique papers — "Why we should not make mean log of wealth big".

