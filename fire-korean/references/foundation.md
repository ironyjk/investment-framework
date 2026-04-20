# FIRE for Korea (Korean-Style Financial Independence and Early Retirement) -- Theoretical Foundation

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

