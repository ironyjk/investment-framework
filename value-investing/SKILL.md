---
name: value-investing
version: "0.2.0"
description: "Value Investing (Graham, Buffett, Munger) — Buy assets undervalued relative to intrinsic value with a margin of safety. The Mr. Market metaphor. Combining quantitative (PBR·PER·FCF) and qualitative (moat·management) analysis."
---

# Value Investing

> Background and theory: Read references/foundation.md



## When to Use

- Valuing individual companies / stocks
- When you need to judge "cheap/expensive"
- When the overall market feels overvalued (searching for undervalued sectors)
- When you actually have the time and interest to analyze companies
- When you prefer a concentrated (few-stock) investment style

## Practical Application

### Value Investing Checklist (Simplified)

```
[Quantitative]
- PER: Is it low relative to industry and historical average?
- PBR: Is it undervalued relative to assets?
- FCF Yield (free cash flow / market cap) > 5%
- Debt ratio < 100%, interest coverage ratio > 5
- 10-year average ROE > 15%

[Qualitative]
- How does it make money (in one sentence)?
- Will it still exist in 5 years?
- Is there a point that competitors find hard to attack (moat)?
- Is management shareholder-friendly (dividends, buybacks, salary / stock-option abuse)?
- Do *you* understand this business?

[Margin of Safety]
- Conservative DCF estimate → Is the current price below 60% of intrinsic value?
```

### Value Investing Style Spectrum

| Style | Representative | Characteristics |
|---|---|---|
| Deep Value | Graham, early Buffett | Based on liquidation value, cigar butt |
| Quality Value | Late Buffett, Munger | Good companies with moats at fair prices |
| Growth-at-a-Reasonable-Price (GARP) | Peter Lynch | PEG < 1 |
| Magic Formula | Greenblatt | Quantitative screening |
| Contrarian | Dreman | Sectors / stocks the market hates |

## Korean Context

### 1. Constraints on Value Investing in the Korean Stock Market

- **Korea Discount**: The average PBR of Korean companies is structurally low. Risky to mechanically apply "low = cheap."
- **Governance Risk**: Chaebol governance, tunneling, and private benefit extraction delay the realization of intrinsic value
- **Low Dividend Payout**: Korean average payout ratio is 20–25% (US 40%+). Weak channel for FCF to return to shareholders.
- **Insufficient Share Buyback Cancellation**: Even when companies buy back shares, they hold rather than cancel them → used to defend controlling shareholders' management rights

### 2. Application Points for Korean Value Investing

- Prefer stocks combining **low PBR + share buyback cancellation / expanded dividends** (overlaps with activist fund targets)
- **Corporate Value-Up Program** (2024~): Mandatory disclosure of corporate value enhancement plans. Launch of the "KRX Korea Value-Up Index" in November 2024, with related ETFs listed (KODEX/TIGER/ACE Value-Up index-tracking). As of 2026, debate over effectiveness continues — *initial short-term performance has been limited; long-term structural improvement is still being observed*
- **Commercial Act amendment discussions** (2024–2025): Adding shareholders to the scope of directors' fiduciary duty → strengthening protection of general shareholders. As of April 2026, need to check the status of the amendment bill pending in the National Assembly.
- **Holding Company Discount**: Holding companies trade at 40–60% discount to NAV. Examine recovery triggers (spin-offs, share buyback cancellation, dividend expansion)
- **Preferred Share Discount**: Some preferred shares trade at 40%+ discount to common shares with more favorable dividends — an entry point for small-scale value investors. Caveat: liquidity and voting-right issues.
- **Caution**: Value-Up themed ETFs are more "low PBR + capital efficiency screeners" than "value investing." Because they involve index inclusion/exclusion turnover and rule-based rebalancing, they differ from Graham-style value investing (→ closer to `factor-investing`).

### 3. Cautions for Calculating "Intrinsic Value" Korean-Style

- Net income volatility is high → use 5–10 year average earnings
- Consolidated vs. standalone financial statements → large share of subsidiaries and affiliates
- Low-liquidity small/mid caps → spreads and transaction costs erode margin of safety

## Anti-Patterns & Overapplication

- **Buying because it's cheap** — "Value trap" — a failing company looks cheap
- **Buying by lowest PER** — Mechanical application failure ignoring industry characteristics and earnings quality
- **Imitating Buffett** — Buffett's information access, capital base, and corporate control abilities cannot be replicated by individuals
- **Blind faith in long-term holding** — Rationalizing a company whose value is deteriorating as "long-term holding"
- **Confirmation bias** — Overconfidence in one's own analysis. Seeking only confirming information. (→ `behavioral-biases`)
- **"I understand it" delusion** — Using Buffett's Circle of Competence as a weapon to rationalize one's own biases. Understanding a business and having an investment edge are separate.
- **Value investor's re-entry into a value trap** — "Now that it's cheaper, I'll buy more" into a losing position → averaging down on a truly failing company
- **Abuse of concentrated investing** — Misusing "Buffett concentrates" as grounds for an individual to go all-in on 3 stocks
- **Quantitative only, ignoring qualitative** — Magic Formula works on average, but has large variance for individual stocks

## Limitations

1. **Information asymmetry** — Individuals are disadvantaged in real-time information compared to institutions and hedge funds
2. **Time consumption** — 10–40 hours to properly analyze one stock. Cost of running a portfolio.
3. **Delay in value realization** — Even after discovering "cheap," it takes 3–10 years for the market to recognize it
4. **Value vs. Growth over the past 20 years**: From 2010–2020, Value lost to Growth over the long term. Debate over factor collapse.
5. **EMH rebuttal**: The Bogleheads camp argues that value investing's excess returns are luck or have disappeared
6. **Behavioral difficulty**: Buying stocks the crowd hates → sustained losses for 6 months to 2 years → most people cannot endure it

## Frameworks to Use Alongside This One

- `factor-investing` — Value is one factor in factor investing (HML, Fama-French)
- `kelly-criterion` — Determining position size per stock
- `behavioral-biases` — Biases value investors should especially watch for
- `korean-tax-optimization` — Utilizing long-term holding tax benefits

## When This Framework Is *Wrong*

- No time, interest, or analytical capacity → `bogleheads`
- Whole-market structural analysis → `modern-portfolio-theory` / `all-weather`
- Systematic factor-based approach → `factor-investing`
- Bear-market defense → `all-weather` / `barbell-strategy`

## Further Reading

- Graham, B. (1973). *The Intelligent Investor* (4th ed.). — Essential reading.
- Graham, B. & Dodd, D. (1934). *Security Analysis*. — The original text, high difficulty.
- Greenblatt, J. (2005). *The Little Book That Still Beats the Market*. — Magic Formula.
- Dorsey, P. (2004). *The Five Rules for Successful Stock Investing*. — Morningstar moat framework.
- Korean application: Writings by domestic value investors such as Kang Bang-cheon, Park Young-ok, and Choi Jun-chul.
- Buffett's shareholder letters (berkshirehathaway.com/letters) — Free, the most practical textbook.

