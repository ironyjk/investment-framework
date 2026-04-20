---
name: all-weather
version: "0.2.0"
description: "All Weather Portfolio (Ray Dalio, Bridgewater) — diversifies across assets that perform well in each of the four economic quadrants (growth ↑/↓ × inflation ↑/↓) using equal risk contribution. Based on the Risk Parity concept. Prepares for every environment rather than predicting."
---

# All Weather Portfolio

> Background and theory: Read references/foundation.md



## When to Use

- "I have no idea where or when the market is going" — a strategy for prediction abstainers
- When **downside defense** is the goal
- Withdrawal-phase (post-retirement) portfolios — when there is no time to recover after a major drawdown
- Investors who cannot emotionally endure heavy volatility
- When asset size has grown so that "preservation" matters more than "accumulation"

## Practical Application

### All Weather Example for Korean Investors (Not a Recommendation)

| Asset | Weight | Example Korean Tickers |
|---|---|---|
| Long-term US Treasuries | 40% | TLT (direct purchase) / KODEX US Ultra 30Y Treasury Futures |
| Intermediate US Treasuries / Korean Treasuries | 15% | IEF / KODEX 10Y KTB |
| Equities (global) | 30% | VT / VTI / KODEX US S&P500 |
| Gold | 7.5% | GLD / KODEX Gold Futures (H) |
| Commodities | 7.5% | DBC / KODEX WTI Crude Futures (watch out for rollover costs) |

- **Choice of FX hedging required**: FX exposure on US Treasuries is an unintended risk
- Verify **ETF expense ratios** (domestic versions have lower fees and different tax treatment)

## Korean Context

### 1. Why All Weather Is Difficult for Korean Investors

- **Access to long-duration US Treasuries**: direct-buying overseas ETFs (TLT) incurs 22% capital gains tax and FX risk
- **Commodity ETFs**: Korean commodity ETFs are inefficient for long-term holding due to *futures rollover costs*
- **KRW vs. USD**: dollar assets are resilient in crises, but domestic consumption and real estate in Korea are in KRW — FX weighting must be designed deliberately
- **Interest rate regime shift**: the bond bull market that lasted until 2020 is unlikely to repeat after 2022 — the 55% bond weight warrants reassessment

### 2. Variants for Korean Investors

- Replace part of US Treasuries → Korean government bonds / FX-hedged US Treasury ETFs
- Reduce commodity weight (5%), increase gold weight (KRX physical gold has favorable tax treatment in Korea)
- Consider raising equity weight (30→40) — for investors in the accumulation phase

### 3. Taxation

- Domestic bond ETFs: 15.4% tax on dividend/interest income
- Overseas bond ETFs (direct purchase): 22% capital gains tax, 15% on dividends
- Physical gold (KRX): favorable dividend/capital gains tax treatment for long-term holding ← see `korean-tax-optimization`

## Anti-Patterns & Overapplication

- **Packaging with past returns** — All Weather performed well from 2000–2020 partly because of a *bond bull market*. It looks different in a rising rate regime.
- **55% bonds in a low-rate environment** — breaks hard in a bond crash like 2022. It actually did break.
- **"Invincible portfolio" misconception** — All Weather is a *less breakable* portfolio, not an unbreakable one
- **Excessive application during accumulation** — someone in their 30s using All Weather will have returns too low, risking insufficient retirement funds
- **Risk Parity leverage in retail accounts** — the leverage institutions use poses bankruptcy risk in personal accounts

## Lessons from the 2022 Failure Case

All Weather's biggest crisis in 2022:
- Annual performance roughly -20% (long-term Treasuries -30%+, equities -18%, gold -1%)
- Cause: **simultaneous rise in inflation + rate hikes** — in Dalio's "growth ↓ · inflation ↑" quadrant, bonds and equities **broke together**
- The first correlation spike since 1970s stagflation (the equity-bond negative diversification benefit disappeared)
- Lesson 1: **Bonds are not always a safe asset** — in rising rate regimes they fall alongside equities
- Lesson 2: **TIPS, commodity, and gold weights may have become more important** (inflation defense)
- Lesson 3: **Dalio himself signaled portfolio adjustments from 2023 onward** — acknowledging a regime shift
- Retail application: understand 2020s All Weather with the **55% bond weight as a regime-dependent variable, not a fixed value**

## Limitations

1. **Bond dependency** — designed on the assumption of a bond bull market. In rising rate regimes, bonds are not a safe asset.
2. **Low expected return** — CAGR is 1–2pp lower than 60/40 or 100% equities over the long run.
3. **Incomplete inflation hedge** — 15% in gold·commodities is insufficient defense against hyperinflation.
4. **Tail risk not reflected** — like MPT, assumes a normal distribution — (→ see `barbell-strategy` alternative).
5. **After Korean taxes** — high weight in foreign assets·dollar exposure leads to underperformance under Korean tax treatment.
6. **Complexity** — requires rebalancing 5–7 asset classes to target weights. Execution costs and potential mistakes.

## Use Alongside

- `modern-portfolio-theory` — theoretical foundation of All Weather
- `rebalancing` — essential to maintain the four-quadrant balance
- `barbell-strategy` — All Weather is "less breakable" asset allocation; Barbell is "profitable even when broken"
- `korean-tax-optimization` — recalculate after-tax returns

## When This Framework Is *Wrong*

- Accumulation phase · young investors (insufficient expected return) → `bogleheads` + higher equity weight
- Preparing for extreme tail risk → `barbell-strategy`
- Individual stock evaluation → `value-investing` / `factor-investing`
- Active return pursuit → `factor-investing`

## Further Reading

- Dalio, R. (2017). *Principles: Life and Work*. (focused on philosophy and principles)
- Bridgewater "Engineering Targeted Returns and Risks" (Bridgewater public report)
- Qian, E. (2016). *Risk Parity Fundamentals*.
- Korean application discussions: asset allocation books by Hong Chun-uk, Kim Sung-il, and others (variants adapted for Korean taxation and FX)
- Critique: Antti Ilmanen *Expected Returns* — discusses the limits of All Weather after the end of the bond bull market.

