---
name: fire-korean
version: "0.1.0"
description: "Korean-style FIRE (Financial Independence, Retire Early) — adapting the 4% rule to Korea, with real estate weighting, National Pension (국민연금), health insurance premium (건보료), pension savings (연금저축) crossover, the pension crevasse (ages 55–65), and path design reflecting Korea-specific variables."
---

# FIRE for Korea (Korean-Style Financial Independence and Early Retirement)

## One-Line Summary

**The U.S. FIRE formula cannot be applied directly to Korea.** You must factor in real estate weighting, National Pension (국민연금), health insurance premium (건보료), the timing of pension savings (연금저축)·IRP withdrawals, and the "pension crevasse" between ages 55–65. The mainstream view is that the 4% rule is closer to a *3–3.5% rule in Korea*.

## Theoretical Origins

- **William Bengen (1994)** — "Determining Withdrawal Rates Using Historical Data." The original 4% rule.
- **Trinity Study (1998)** — Cooley, Hubbard, Walz. Analyzed the 30-year success rate of 4% withdrawals from a 50% stock / 50% bond portfolio.
- **Vicki Robin, Joe Dominguez** *Your Money or Your Life* (1992) — Ideological root of the FIRE movement.
- **MMM (Mr. Money Mustache)** blog (2011~) — Popularized FIRE.
- Korean adaptation discussions: Modified applications by domestic FIRE authors such as Kang Hwan-kook and Kim Seong-il.

## FIRE Basic Formulas

### 1. The 4% Rule

$$\text{Required Assets} = \text{Annual Spending} \times 25$$

- Withdraw 4% of retirement assets each year (inflation-linked)
- 30-year success rate for a 50/50 portfolio ≈ 95% (based on historical U.S. data)
- Example: ₩40M annual spending → ₩1B required

### 2. FIRE Variants

- **Lean FIRE**: Bare-bones living standard (₩20–30M annual spending, ₩600–800M)
- **Fat FIRE**: Comfortable retirement (₩80M–100M+, ₩2B+)
- **Barista FIRE**: Combined with part-time work, not full retirement
- **Coast FIRE**: Reaching traditional retirement age through compounding alone, without additional saving

### 3. Reviewing the Safe Withdrawal Rate (SWR)

- Bengen himself later revised upward to 4.5–4.7% (portfolios including growth stocks)
- Recent research: **3–3.5%** is safer in an era of low interest rates and high valuations (Blanchett, Finke)
- **Conservative when applied to Korea**: 3–3.5% recommended

## Korea-Specific FIRE Variables

### 1. National Pension (Public Pension)

- **Payment commencement**: Age 61 for those born 1953–56 / Age 62 for 1957–60 / Age 63 for 1961–64 / Age 64 for 1965–68 / **Age 65 for those born 1969 onward** (phased increase)
- **Average benefit**: As of 2025, the average old-age pension is approximately ₩600,000–650,000/month (varies by contribution period and amount, per National Pension Service disclosures — *verification needed, updated annually*)
- **For 20+ year contributors**: ₩1,000,000–1,500,000/month is common
- **From a FIRE perspective**: Since this is a *guaranteed cash flow* after age 65, it has the effect of reducing the required asset size
- **Check expected benefits**: National Pension Service website

### 2. Retirement Pension / IRP

- Retirement allowances can mostly be transferred to an IRP
- When received as pension after age 55, the tax rate is 3.3–5.5% (low)
- **From a FIRE perspective**: IRP + pension savings (연금저축) combined at ₩9M × 20 years = ₩180M+ accumulated (effective amount larger when tax credits are included)
- **Central to solving the crevasse**

### 3. Health Insurance (건보료)

- **Dependent status retention criteria (Sept 2022 reform, as of April 2026)** — loss of status if any one is violated:
  - Combined annual income (earned, business, pension, financial, other) of **₩20M or less**
  - **If financial income (interest + dividends) exceeds ₩10M per year, the entire amount is recognized as income** — treated as 0 if ₩10M or below
  - Property tax base of **₩540M or less** (loss of status if property exceeds ₩540M AND income exceeds ₩10M)
  - **Loss of status regardless of income if property tax base exceeds ₩900M**
  - Loss of status if business income arises
- Upon loss of status, as a **regional subscriber**: monthly burden of ₩200,000–600,000 based on income and property
- **Whether dependent status can be maintained is a key variable when executing FIRE**
- When designing withdrawal rates, mind the health insurance premium (건보료) boundaries (especially the ₩10M financial income threshold)

### 4. Real Estate Weighting

- Most Korean FIRE practitioners combine **homeownership + financial assets**
- For homeowners, no rent outlay → annual spending of ₩20–30M possible (Lean FIRE)
- However, property tax, management fees, and repair costs must be factored in
- **Reverse mortgage (주택연금)** available: aged 60+ with owned home, lifetime monthly payments

### 5. The Pension Crevasse, Ages 55–65

- Korean public pensions begin at ages 63–65
- In early retirement, **the 10-year stretch between ages 55 and 65 is the biggest challenge**
- During this period, financial assets are withdrawn purely
- **Solution**: Prepare a separate bucket (cash·short-term bonds) for this period

### 6. Life Expectancy and Retirement Duration

- Korean life expectancy (2023 life table, announced by Statistics Korea in 2024): Male 80.6 / Female 86.4 (*updated annually — verification needed*)
- Retiring at 55 → 25–35 years of withdrawals
- May exceed the Trinity 30-year basis → 3% rule more strongly recommended

## Recalculated Korean-Style SWR

| Scenario | U.S. 4% Rule | Korea Recommended | Rationale |
|---|---|---|---|
| Traditional retirement (age 65, 30-year withdrawals) | 4.0% | 3.5–4.0% | Trinity + Korean life expectancy + low-yield environment |
| Early retirement (age 55, 40-year withdrawals) | 3.3% | **3.0%** | Blanchett (2013) · Pfau (2012) low-rate adjustment |
| Ultra-early (age 45, 50-year withdrawals) | 3.0% | **2.5–3.0%** | 50-year Monte Carlo · Sequence risk |
| Homeownership + National Pension factored in | — | **Reduces required assets by 25–35%** | National Pension PV + elimination of rent outlays |

**Variables that must be incorporated in SWR calculation**:
- Sources for expected-return (μ) and volatility (σ) assumptions
- Inflation assumption (whether a 2.0–2.5% long-run Korean average is reasonable)
- Sequence-of-returns risk (market environment in the first 10 years)
- Rising medical and long-term care expense trends
- Scenarios for National Pension payment rate reform (discussions of 2055 fund depletion, risks of rate cuts and later commencement)

→ For ₩50M annual spending, homeownership, and expected National Pension of ₩1M/month:
- Pure 4% rule: ₩1.25B required
- Korean-style adjusted: **₩700M–900M** is also feasible (National Pension + homeownership)

## Designing a Korean-Style FIRE Path

### Accumulation (20s·30s)
1. **Maximize savings rate**: Target 50%+ of take-home pay
2. **Fully fund pension savings (연금저축)·IRP limits** (₩9M/year)
3. **Use the ISA ₩20M annual limit**
4. **Equity index weighting of 70–80%** (→ `bogleheads`)
5. **Home purchase vs. savings/investment comparison** (life-cycle perspective, varies by region)

### Mid-Accumulation (late 30s–40s)
1. **Rebalance asset allocation** (→ `rebalancing`)
2. **Review real estate / financial asset weighting** (→ `modern-portfolio-theory`)
3. **Calculate FIRE target size + design the crevasse bucket**
4. **Leverage peak earned income — private education vs. savings trade-off** (may be linked to Ulsan education environment issues)

### Pre-Retirement (final 5 years before FIRE)
1. **Shift to conservative asset allocation** (equities 60→40–50)
2. **Cash flow plan through age 55** (pre-pension-commencement period)
3. **Health insurance premium (건보료) design** — minimize the structure of income recognition
4. **Prepare for sequence-of-returns risk** — a drawdown in the first 5 years is fatal

### Post-Retirement (Withdrawal Phase)
1. **Bucket Strategy (linked to Korean tax structure)**:
   - **Bucket 1 (2–3 years of living expenses)**: Cash·MMF·time deposits — general account (liquidity first)
   - **Bucket 2 (5–7 years)**: Short·medium-term Treasury ETFs·dividend ETFs — operated within ISA (separate taxation·₩2M tax-free)
   - **Bucket 3 (remainder, long-term growth)**: Global equity index — pension savings (연금저축)/IRP (3.3–5.5% tax rate from age 55+)
   - **Withdrawal order**: Bucket 1 → dividends/distributions → Bucket 2 → Bucket 3 (reverse order of tax rates)
   - **Maintaining the dependent-status boundary**: If pension savings (연금저축) withdrawals are ₩15M or less per year, separate taxation applies, improving likelihood of retaining health insurance (건보료) dependent status
   - For early retirement before age 55: pension accounts inaccessible → Buckets 1·2 must last until age 55 (the crevasse)
2. **Dynamic withdrawal rate (Guyton-Klinger Rules)**:
   - **Capital Preservation Rule**: Cut withdrawals by 10% if the current withdrawal rate exceeds 120% of the initial (case where weighting grew after a market drop)
   - **Prosperity Rule**: Raise withdrawals by 10% if the rate falls to 80% or less of the initial
   - **Withdrawal Rule**: Freeze inflation adjustment if prior-year portfolio return was negative
   - **Portfolio Management Rule**: Sell appreciating assets first (preserve depressed assets)
   - Korean version: Add maintenance of health insurance premium (건보료) dependent-status boundaries (₩20M annual / ₩10M financial) as an additional constraint
3. **Solving the pension crevasse**: Concentrate financial-asset withdrawals between ages 55–63, then lower the withdrawal rate via National Pension from age 63+

## Korea-Specific Family Structure (Reflecting User Context)

- **Uncertainty in child education expenses**: ±₩300–500M in required assets depending on university·study abroad support
- **Residential changes such as moving out of Ulsan**: Real estate asset revaluation needed
- **Scenario of ₩180M earned-income wage-earner × 3 children**:
  - Estimated after-tax take-home ₩120–130M/year (based on 2026 taxation·4 major insurances·local tax)
  - Child-rearing costs for 3 (including private education) ₩40–60M/year
  - Housing costs (management fees·property tax·loan interest) ₩15–25M/year
  - Basic living expenses ₩30–40M/year
  - **Remaining savings potential ₩30–50M/year** (ideal case; actual varies widely)
  - 10-year compounded (4% real return assumption) accumulation: ₩400–600M in financial assets
  - **Realistic FIRE target**: Coast FIRE at age 45–50 + National Pension·homeownership + retirement in early 60s
- **Three-child specifics**: Considering education costs·independence support (marriage·housing), *Lean FIRE is unrealistic*. **Coast FIRE or Barista FIRE** is reasonable.
- **Ulsan trade-up funds = short-term liquidity bucket**. Separate from the investment portfolio and hold in MMF·short-term bonds·deposits.

### Simulation Example (Not a Recommendation, for Structural Understanding)

```
Current (2026):
- Annual income ₩180M, after-tax ₩125M, annual savings ₩40M
- Financial assets assumption: ₩200M (pension + ISA + general)
- Homeownership market value assumption: ₩700M (Ulsan), loan ₩200M

Target: Barista FIRE (partial retirement) at age 55
  - Required funds at age 55 = Annual spending × 25 × 0.7 (National Pension·homeownership adjustment)
  - Assuming ₩50M annual spending → ₩875M asset target

Path:
  - Over next 15 years, annual savings ₩40M + 6% compounding
  - FV = ₩200M × 1.06^15 + ₩40M × ((1.06^15-1)/0.06)
  - ≈ ₩480M + ₩930M = ₩1.4B (nominal)
  - Real (adjusted for 2.5% inflation) ≈ ₩970M → within target range

Risks:
  - -₩200–500M if supporting children for university·study abroad
  - Drawdown sequence risk (40% drop just before age 55)
  - Real estate asset fluctuation during trade-up
  - Earned-income interruption risk (layoff·health)
```

*This is an example for structural explanation; the actual plan must be recalculated annually. All numbers are assumptions.*

## Anti-Patterns & Over-Application

- **Copy-pasting the U.S. 4% rule** — Does not reflect Korean low rates·aging
- **Ignoring National Pension** — Over-saving if excluded from asset calculation
- **Calculating without real estate** — The homeownership effect in Korea is large
- **Lean FIRE obsession** — Extreme frugality → burnout → many cases of abandoning FIRE
- **Designing for zero earned income** — Having some work, like Barista FIRE, is often advantageous psychologically·for health insurance premium (건보료)·and risk-wise
- **Lean FIRE target with three children** — Unrealistic. Revisit as Fat FIRE or Coast FIRE
- **Single-market concentration** — Attempting FIRE with 100% Korean equities → vulnerable to Japan-style long-term stagnation
- **Concentrated selling at retirement point** — Simultaneous hit from massive capital gains tax·health insurance premium (건보료)

## Limitations

1. **Future institutional uncertainty** — National Pension payment rate·commencement age·tax system all subject to change
2. **Inflation scenarios** — SWR validity shakes under high inflation
3. **Medical expenses unpredictable** — Elderly medical expenses are the greatest uncertainty in FIRE calculations
4. **Scope of child support** — Whether to support marriage·housing makes hundreds-of-millions difference
5. **Psychological difficulty** — Loss of meaning·identity after FIRE achievement (post-FIRE depression)
6. **Empirical basis of the 4% rule**: U.S. 20th-century data. Korean empirical data is scarce
7. **Influence of Korean real estate cycles**: If 70% of assets are in real estate, the housing cycle dominates FIRE as a whole

## What to Use with This Framework

- `bogleheads` — Standard engine for FIRE accumulation
- `korean-tax-optimization` — Account structure design
- `rebalancing` — Bucket rebalancing in the withdrawal phase
- `all-weather` — Defensive allocation in the withdrawal phase
- `dollar-cost-averaging` — Accumulation automation
- `behavioral-biases` — Psychological structure for 20+ year persistence

## When This Framework Is *Wrong*

- Assets under ₩100–200M — *Raising the savings rate itself* comes first, before FIRE calculations
- Self-employed·small business → income volatility must be considered separately. Simple 4% rule inapplicable.
- 90%+ real estate concentration → design separately with the `realty` framework
- Extreme volatility aversion → *working longer* may be psychologically better than Lean FIRE

## Further Study

- Bengen, W. (1994). "Determining Withdrawal Rates Using Historical Data."
- Cooley, Hubbard, Walz. "Trinity Study" (1998).
- Blanchett, D. & Finke, M. — Modern SWR review papers.
- Robin, V. & Dominguez, J. *Your Money or Your Life*.
- Korean adaptations:
  - Kang Hwan-kook *You Can Do It! Quant Investing*, *Portfolio of Giants* — Korean backtested FIRE
  - Kim Seong-il *The Magic of Rolling Money*
  - Park Gomhee YouTube — Korean FIRE practice
- National Pension Service Retirement Preparation Service — Official expected benefits inquiry
- **Note**: All figures are as of April 2026. The system·tax code·pension commencement age are all subject to change.
