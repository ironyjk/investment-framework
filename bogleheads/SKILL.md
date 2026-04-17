---
name: bogleheads
version: "0.1.0"
description: "Bogleheads philosophy (John Bogle, Vanguard) — low-cost index investing, 3-fund portfolio, efficient market hypothesis, costs as the only certain alpha. 'Don't look for the needle in the haystack — buy the haystack.'"
---

# Bogleheads Philosophy

## One-Line Summary

**"Don't try to beat the market — buy the market."** Returns are unpredictable, but *costs are certain*. Holding the entire global market through 2–3 low-cost index funds is the rational default for individual investors.

## Theoretical Origins

- **John C. Bogle** (1929–2019) — Founded Vanguard (1975), launched the world's first publicly available index fund (S&P500) in 1976.
- **Eugene Fama** — Efficient Market Hypothesis (EMH, 1970). "Market prices already reflect all available information."
- **Burton Malkiel** — *A Random Walk Down Wall Street* (1973). The popularizing classic.
- **SPIVA Reports** (S&P) — Year after year, empirically demonstrate that most active funds lose to their benchmark on a 15-year cumulative basis.

## Core Principles

### 1. Cost Matters Hypothesis (Bogle)

- *"Market return – costs = investor return"*
- A 1 percentage point difference in fees erodes 25–30% of assets cumulatively over 30 years
- For an active fund to beat the index, it must generate alpha exceeding the cost gap (0.5–1.5%) → structurally difficult

### 2. 3-Fund Portfolio (Taylor Larimore)

- **Domestic total market stocks**
- **International total market stocks**
- **Total bond market**
- Simple, but covers 99% of global assets. Rebalancing is straightforward.

### 3. Make Time Your Ally

- The longer the investment horizon, the safer a higher equity allocation
- **Age ≈ bond allocation** or **(120 − age) = equity allocation** — rough rules of thumb (popular formulas proposed within the Bogle camp; many today criticize these as conservative and relax them to reflect extended life expectancy)
- Sequence-of-returns risk is severe only during the withdrawal phase → in the accumulation phase, even 100% equity is considered reasonable by some

### 4. Stay the Course

- No market timing attempts (the most important behavioral rule)
- Ignore news and forecasters
- *Not selling* during a downturn is the greatest skill

### 5. Cost Priority Order
1. Expense Ratio
2. Transaction costs and bid-ask spreads
3. Taxes (potentially the largest item)
4. Behavioral costs (emotional trading)

## When to Use

- **Investing beginners** — Minimize complex decisions
- **Busy working professionals** — Minimize management time
- When you *don't* have conviction that "I can beat the market" (and even when you do, you're usually wrong)
- Below-mid asset levels (under several hundred million KRW) — tax optimization complexity rises with scale
- Long-term investing (15+ years)

## Practical Application

### 3-Fund for Korean Investors (illustrative, not a recommendation)

| Asset | Example Weight | Example ETFs |
|---|---|---|
| International total market stocks | 50–60% | VT / VTI + VXUS / KODEX U.S. S&P500 / TIGER U.S. Nasdaq100 |
| Domestic stocks | 10–20% | KODEX 200 / TIGER KRX300 |
| Bonds | 20–40% (depending on age/goal) | KODEX 10Y KTB / TIGER U.S. 10Y Treasury Futures |

### Execution Steps

```
1. Decide asset allocation (age, goal, risk tolerance)
2. Choose the lowest-fee index ETFs
   - Korean-listed 0.1–0.3%, direct overseas purchase 0.03–0.1%
3. Account priority:
   pension savings (연금저축)/IRP → ISA → general brokerage (in order of tax efficiency)
4. Buy fixed amounts via monthly auto-transfer (→ `dollar-cost-averaging`)
5. Rebalance once a year (→ `rebalancing`)
6. Otherwise, *do nothing*
```

## Korean Context

### 1. Advantages of Executing Bogleheads in Korea
- Pairs well with tax-advantaged accounts (ISA, pension savings (연금저축), IRP) — low turnover and long holding maximize tax benefits
- The opposite of Korea's individual stock-trading culture → a differentiated edge
- As of 2026, Korean ETF fees have dropped to 0.1–0.3% (still higher than the U.S. 0.03–0.1%)

### 2. Korea-Specific Considerations
- **Korean active fund performance**: SPIVA Korea reports show 70–90% of active funds lose to the benchmark on a 10–15 year basis — the same pattern as the U.S.
- **22% capital gains tax on direct overseas stocks**: Tax is triggered at sale → long-term holding produces tax deferral
- **Korean-listed overseas equity ETFs**: 15.4% on dividends + 15.4% dividend income tax on capital gains — a different structure. Tax comparison is essential (→ `korean-tax-optimization`)
- **FX**: Overseas ETFs like VT carry currency exposure. KRW-converted volatility increases.

### 3. Korean Adaptations of Boglehead Philosophy

- **Lazy Portfolio** Korean version: Just two ETFs — an S&P500 ETF + a Korean bond ETF — can implement the basics
- **Whole-balance-sheet view**: For Korean households dominated by real estate, running the entire financial-asset portion as Bogleheads provides relative diversification

## Anti-Patterns & Over-Application

- **"All index funds are the same"** misconception — large differences in fees, tracking error, taxation, liquidity
- **Thematic ETF illusion** — "Semiconductor ETFs" or "Battery ETFs" are not index funds, they are theme bets
- **Leveraged ETFs** — Bogle himself was wary. Daily-reset structure causes decay over long holding periods
- **Indexing only Korean stocks** — Concentration in KOSPI is concentration, not diversification. Global indexing is essential.
- **The misconception that index funds are safe** — Index funds can also fall 50% (2008, 2020)
- **Too many funds** — A 3-fund turning into a 10-fund increases management and rebalancing costs while diversification benefits hit diminishing returns

## Limitations

1. **EMH debate** — No market is perfectly efficient. Anomalies (factors) exist (→ `factor-investing`).
2. **Doesn't work in every era** — Japan's Nikkei index stagnated for 20 years (1990–2010).
3. **Some argue passive is inefficient in emerging markets and small caps** — markets with large information asymmetry.
4. **Hard to apply ESG/ethical filters** — Total market purchases include problematic companies by definition.
5. **Emotionally seems easy but is actually hard** — "Doing nothing" is the hardest part (→ `behavioral-biases`).
6. **Concentration risk exists (intensified in 2025–2026)**: The top 10 names by market cap in the S&P500 make up **35%+** of the index, with MAG7 (Apple, Microsoft, NVDA, Alphabet, Amazon, Meta, Tesla) alone accounting for **30%+**. Concentration is comparable to the 1960s Nifty Fifty and the 1999 dot-com bubble. "500-stock diversification" is nominal — substantively, it is closer to a **mega-cap tech bet**.
   - Mitigation options: Instead of cap-weighted S&P500, use **equal-weight (RSP)** or **global cap-weighted (VT)**. However, the former has higher fees and the latter still has 60%+ U.S. weight.
   - Philosophical caveat: Bogle himself argued "cap weighting defines the market" and did not avoid concentration. But this may not align with an individual investor's psychological tolerance.

## Frameworks That Pair Well With This One

- `modern-portfolio-theory` — Bogleheads is the *minimum-cost implementation* of MPT
- `dollar-cost-averaging` — How you buy the index
- `rebalancing` — Maintaining long-term weights
- `korean-tax-optimization` — Maximizing after-tax returns in Korea
- `fire-korean` — The standard accumulation engine for index-based FIRE

## When This Framework Is *Wrong*

- High-net-worth tax/inheritance complexity → deeper `korean-tax-optimization`
- Conviction that the entire market is overvalued → `value-investing` (though such conviction is usually wrong)
- Preparing for extreme tail risk → `barbell-strategy`
- Behavioral/emotional issues → `behavioral-biases`

## Further Learning

- Bogle, J. (2017). *The Little Book of Common Sense Investing* (revised ed.). — The definitive primer.
- Larimore, T. (2018). *The Bogleheads' Guide to the Three-Fund Portfolio*.
- Malkiel, B. (2019). *A Random Walk Down Wall Street* (12th ed.).
- Online: bogleheads.org forum — the largest community for practical Q&A.
- Korean adaptation: Kim Sung-il, *Magic Money Rolling* (마법의 돈 굴리기) — popular Korean-language asset allocation book.
- SPIVA Reports (spglobal.com/spdji/en/research-insights/spiva/) — Official statistics on active vs. passive.
