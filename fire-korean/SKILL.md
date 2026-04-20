---
name: fire-korean
version: "0.2.0"
description: "Korean-style FIRE (Financial Independence, Retire Early) — adapting the 4% rule to Korea, with real estate weighting, National Pension (국민연금), health insurance premium (건보료), pension savings (연금저축) crossover, the pension crevasse (ages 55–65), and path design reflecting Korea-specific variables."
---

# FIRE for Korea (Korean-Style Financial Independence and Early Retirement)

> Background and theory: Read references/foundation.md



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

