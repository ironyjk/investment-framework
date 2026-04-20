---
name: factor-investing
version: "0.2.0"
description: "Factor Investing (Fama-French 3/5 factor) — explaining excess returns through a small number of systematic 'factors': Value, Size, Momentum, Quality, Low-Vol. The theoretical foundation of smart-beta ETFs. A substitute for individual stock analysis."
---

# Factor Investing

> Background and theory: Read references/foundation.md



## When to Use It

- When Bogleheads (market index) alone feels insufficient.
- When you lack the time or ability for individual stock analysis but *still want excess returns*.
- Diagnosing factor exposure in your portfolio (am I already over-exposed to a particular factor?).
- As a criterion for selecting smart-beta ETFs.
- Systematic investing at the institutional / pension fund level.

## Practical Application

### Smart-Beta ETF Examples (not recommendations — educational examples of products exposed to each factor)

| Factor | U.S. ETF | Domestic ETF (if available) |
|---|---|---|
| Value | VLUE, IUSV | TIGER 미국가치 |
| Size (Small) | VB, IJR | KODEX 코스닥150 |
| Momentum | MTUM | – (limited) |
| Quality | QUAL, DGRO | TIGER 미국퀄리티배당 |
| Low-Vol | USMV, SPLV | KODEX 미국S&P500 저변동성 |
| Multi-factor | DFAX, GSLC | – |

### Factor Portfolio Example (Equal-weight multi-factor)

```
Total Market: 40%
Value factor: 15%
Quality factor: 15%
Momentum factor: 10%
Small-cap: 10%
Low-vol: 10%
```

### Dimensional Fund Advisors (DFA) / Avantis Approach

- Fund managers built on the original Fama-French research.
- Scientifically designed factor tilts with low costs.
- Individual access is limited, but the philosophy is worth studying.

## Korean Context

### 1. Factor Validity in the Korean Market
- **Value**: Historically a strong factor in Korea (Korea discount + episodes of value-stock rebounds).
- **Momentum**: High volatility in the Korean market creates significant factor noise.
- **Small**: KOSDAQ small/mid caps historically delivered excess returns, but recently diminished.
- **Quality**: Relatively effective since 2020.

### 2. Constraints on Domestic Factor ETFs

- Limited product variety (roughly 1/10 of the U.S. offering).
- Relatively high expense ratios (0.3–0.5%).
- Small AUM leads to liquidity issues.
- When buying foreign factor ETFs directly, FX and tax considerations are required.

### 3. Factor Strategies for Korean Investors

- Combining **direct purchase of global factor ETFs** with **domestic value/dividend ETFs**.
- **Beneficiaries of the Value-Up program (밸류업 프로그램)** = a Korean-style Value+Quality hybrid.
- **Small-cap tilts** are constrained in Korea by liquidity and tax issues (capital gains tax on major shareholders).

## Anti-Patterns & Over-Application

- **All-in on a single factor** — a 100% Value portfolio lost to the market over 2010–2020.
- **Factor timing** — predicting "now is the time for Value" generally fails.
- **Extrapolating past premia** — assuming long-run factor premia persist into the future is risky.
- **"Factors always win"** — factors also have 10–15 year stretches of underperformance.
- **Factor over-mixing** — combining 5 or 10 factors ultimately resembles the market index while only raising costs.
- **Data mining (Factor Zoo)**: academia has discovered 300+ factors, most of which cannot be reproduced in live trading.
  - Harvey, Liu, Zhu (2016): the t-statistic threshold should be raised to **at least 3.0**, not the traditional 2.0, to qualify as a genuine factor.
  - McLean & Pontiff (2016): after academic publication, premia fall by an average of **32%**, and by **58%** post-publication.
  - Bailey & López de Prado (2014): calculates the probability that a significant p-value is a false positive after n backtest trials (deflated Sharpe).
  - **Application for individual investors**: when looking at a new factor or themed ETF, first ask, "Am I one of thousands of researchers who have looked at this data?"

## Limitations

1. **Debate over shrinking factor premia** — research indicating premia fall by more than half after academic publication (McLean-Pontiff).
2. **Transaction costs and taxes** — higher rebalancing frequency erodes factor premia.
3. **Long underperformance stretches** — Value in the 2010s, Momentum's 2009 reversal, etc.
4. **Single-country / single-period bias** — centered on U.S. data. Some factors are weak in other markets or periods.
5. **Execution slippage** — for small-cap / low-liquidity factors, much of the premium evaporates in actual trading.
6. **Inconsistent factor definitions** — Value computed via P/B, P/E, or EV/EBIT produces different performance.

## Works Well With

- `modern-portfolio-theory` — factors are a systematic extension of the MPT frame.
- `bogleheads` — Bogleheads with factor tilts = "Fama-French Boglehead."
- `value-investing` — the quantitative, systematic version of value investing.
- `rebalancing` — essential for maintaining factor weights.

## When This Framework Is *Wrong*

- No time or interest for factor research → `bogleheads`.
- Goal is analyzing individual companies → `value-investing`.
- Macro asset-allocation problem → `modern-portfolio-theory` / `all-weather`.
- Tail risk → `barbell-strategy`.

## Further Reading

- Fama, E. & French, K. (1993). "Common Risk Factors in the Returns on Stocks and Bonds."
- Fama, E. & French, K. (2015). "A Five-Factor Asset Pricing Model."
- Ang, A. (2014). *Asset Management: A Systematic Approach to Factor Investing*. — a comprehensive textbook.
- Asness, C. et al. "Fact, Fiction, and Value Investing" (AQR research).
- Critique: Harvey, Liu, Zhu (2016). "...and the Cross-Section of Expected Returns." — a critique of the factor zoo.
- Korean application: a small number of domestic introductory books such as Kim Young-seong, *Smart Beta* (스마트베타).

