---
name: dollar-cost-averaging
version: "0.1.0"
description: "Dollar-Cost Averaging (DCA) — buy at fixed intervals with fixed amounts. Diversifies timing-failure risk and controls behavioral bias. Theoretically has lower expected value than Lump-Sum, but offers major advantages in emotional stability and executability."
---

# Dollar-Cost Averaging (DCA)

## One-Line Summary

**"If you don't know when to buy, split your purchases."** Buy fixed amounts at fixed intervals. Offsets the risk of buying at peaks and the risk of panic avoidance through *time diversification*. Not mathematically optimal, but overwhelmingly superior in *executability*.

## Theoretical Origins

- **Benjamin Graham** — introduced in *The Intelligent Investor* ("formula plan").
- Academic research: Constantinides (1979) theoretically proved Lump-Sum is superior. However, ignores psychological/information asymmetry conditions.
- Modern behavioral finance perspective: Thaler, Shefrin — a tool for overcoming regret aversion and loss aversion.
- Vanguard, Morningstar research: historically, Lump-Sum outperforms DCA in 2/3 of cases, but DCA is superior in *volatility and worst-case scenarios*.

## Core Concepts

### 1. The Mathematical Essence
- Rising market trend → Lump-Sum (one-time investment) advantageous
- Sideways/declining market → DCA advantageous
- Effect of **lowering the average purchase price** (buying more shares at lower prices)

### 2. DCA vs Lump-Sum (LSI)
- Vanguard 2012 study: U.S. market 1926–2011, 10-year horizon, **LSI wins with 2/3 probability** (average 2.3%p)
- However, LSI's worst-case drawdown is far larger than DCA's
- **Expected return** favors LSI; **utility** may favor DCA

### 3. DCA's True Value
- Not return enhancement but *behavioral control*
- Blocking the temptation of market timing
- Continuing to buy in a downturn = lowering average price
- Can be automated → minimizing emotional intervention

### 4. Value Averaging (Variant)
- Michael Edleson (1988)
- Adjusts purchase/sale amounts so portfolio value tracks a target growth line
- Buy more on declines, buy less on rises
- Slightly superior to DCA but higher complexity

## When to Use

- **Accumulating monthly from salary** — DCA is the natural structure
- When a lump sum comes in but *the market feels overvalued* — psychological DCA
- First-time investors — when afraid to deploy all at once
- Those with strong volatility fear (→ `behavioral-biases`)
- Long-term asset accumulation (retirement pensions, pension savings (연금저축), ISA)

## Practical Application

### Standard DCA Execution

```
1. Decide a fixed monthly (or bi-weekly) amount
   e.g., 1,000,000 KRW/month buying S&P500 ETF
2. Set up automatic transfers
   - Brokerage auto-investment services (supported by Kookmin, Mirae Asset, Korea Investment, Kiwoom, etc.)
   - Leverage ISA, pension savings (연금저축), IRP auto-purchase
3. Purchase strategy
   - Diversify purchases across multiple ETFs per target allocation weights
4. "Don't quit"
   - The deeper the downturn, the more you must *keep* buying to lower the average price
   - Stopping/reducing destroys the essence of DCA
5. Separate rebalancing
   - DCA is buy-only. Weight adjustments follow separate rules (→ `rebalancing`)
```

### Lump-Sum vs DCA Selection Framework

| Condition | Choice |
|---|---|
| Lump sum already in hand + long-term investment | **LSI** (superior expected value) |
| Lump sum + strong volatility fear | **6–12 month DCA** (psychological stability) |
| Accumulating from monthly salary | **DCA** (natural structure) |
| Market clearly looks like a bubble | **12–24 month DCA + retain some safe assets** |
| No conviction | **DCA** (minimize regret) |

### Period Design
- Too short (≤3 months) → little difference from Lump-Sum
- Too long (3+ years) → excessive opportunity cost
- **6–18 months** is the generally recommended range

## Korean Context

### 1. Benefits of Executing DCA in Korea
- Naturally fits the **salaried-income structure**
- Maximizes tax benefits when combined with ISA, pension savings (연금저축), IRP auto-transfers
- Low transaction fees (domestic ETFs 0.015–0.1%)
- Small-amount auto-purchase possible (fractional share purchases under 1 share supported by some brokerages)

### 2. Korea-Specific DCA Caveats
- **Currency DCA**: DCA on overseas stocks includes a currency-diversification effect. FX gains during KRW strength.
- **Tax cycle**: Overseas stock capital gains tax is calculated on a Jan 1 – Dec 31 basis. Purchase timing doesn't matter, but sale timing can be adjusted.
- **Annual 20M KRW dividend/interest income ceiling**: Even with diversified purchases, if cumulative valuation gains and dividends exceed the ceiling, comprehensive taxation applies. Prioritize ISA and pension accounts.
- **Domestic ETFs don't auto-reinvest dividends**: Distributions are paid out as cash, requiring manual reinvestment → use accounts with auto-reinvestment services.

### 3. Practical Korea-Style DCA Priorities (as of 2026.4)
1. **Pension savings (연금저축) tax credit limit of 6M KRW** → 500K KRW/month auto-transfer
2. **IRP additional 3M KRW** (combined cap with pension savings (연금저축): 9M KRW) → 250K KRW/month auto-transfer
3. **ISA annual 20M KRW limit** (brokerage type) → 1.66M KRW/month auto-transfer (wait after hitting limit)
4. Additional purchases in a regular brokerage account

### 4. ISA Limit Constraints and DCA Design

- ISA annual contribution limit of 20M KRW = structure that **effectively forces DCA**
- Lump-sum 20M at year start → exhausts the year's limit, then 11 months of waiting
- 1.66M/month DCA → full-year diversification + tax benefit + psychological stability
- **At ISA maturity (3+ years), you can utilize up to a cumulative 100M KRW limit** (20M × 5 years), and rolling over to a pension account grants an **additional tax credit of 10% of the converted amount (up to 3M KRW)**
- **Caveat**: In brokerage-type ISAs, capital gains on domestic stocks/ETFs are tax-exempt, but overseas-listed ETFs are not ISA-eligible. Substitute with domestically-listed overseas-tracking ETFs (KODEX S&P500, etc.).

## Anti-Patterns & Over-Application

- **DCA as "waiting"** — "Let's wait until the market drops" is not DCA but timing
- **Stopping in a downturn** — exactly the wrong behavior. Abandoning DCA's core value
- **Weekly/daily DCA** — only increases transaction costs with minimal change in expected value
- **5+ year DCA** — excessive opportunity cost. Complete within 1–2 years recommended
- **Salary DCA with emotional trading** — "This month looks expensive, let's skip" without automation is not DCA
- **Misconception that LSI is always bad** — LSI has mathematical superiority in long-term bull markets

## Limitations

1. **Expected return loss** — average 2–3%p lower than LSI (Vanguard study)
2. **Disadvantage in bull markets** — early purchases are favorable if the market rises consistently
3. **Psychological failure in downturns** — continuing to buy during declines is theory, but actual discontinuation is frequent
4. **Irrationality of fixed amounts** — the price of simplicity compared to Value Averaging
5. **Fixed interval/amount is arbitrary** — "100/month" is not mathematically optimal, chosen for convenience
6. **Second-best for lump-sum holders** — trading opportunity cost for psychological peace

## Used Alongside This Framework

- `bogleheads` — DCA is the standard execution method of Bogleheads
- `behavioral-biases` — DCA's true value is bias control
- `rebalancing` — DCA (buying) and rebalancing (weight adjustment) operate separately
- `korean-tax-optimization` — DCA priorities for tax-advantaged accounts

## When This Framework Is *Wrong*

- Lump sum + long-term + neutral market conditions → Lump-Sum has expected-value advantage
- Short-term speculation/trading purposes → DCA unsuitable
- Position sizing problem → `kelly-criterion`
- Overall market bubble judgment → `value-investing` / `barbell-strategy`

## Further Learning

- Graham, B. (1973). *The Intelligent Investor* — original source of the formula plan.
- Vanguard (2012). "Dollar-cost averaging just means taking risk later." (research white paper)
- Edleson, M. (2006). *Value Averaging*. — original source of the variant version.
- Korean application: domestic brokerage blogs and reports (Mirae Asset, KB, NH) — DCA backtests on Korean ETFs.
