---
name: korean-tax-optimization
version: "0.2.0"
description: "Tax optimization for Korean investors — ISA (general/brokerage/low-income), pension savings (연금저축), IRP, overseas stock capital gains tax, dividend/interest income tax, financial investment tax discussions, health insurance premium (건보료) impact. Account prioritization and after-tax return maximization framework."
---

# Korean Tax Optimization

## One-Line Summary

**In Korea, after-tax returns matter more than nominal returns.** Simply filling tax-advantaged accounts like ISA, pension savings (연금저축), and IRP **in the right order** can preserve 15–30% more of your long-term assets. *Account structure* comes before stock selection.

> Background and theory: Read references/foundation.md

## Account Priority (General Framework)

```
1st Priority: Pension savings tax credit limit (KRW 6 million)
  → Immediate tax credit 13.2–16.5% (KRW 790K–990K annual refund)

2nd Priority: IRP additional tax credit (combined with pension savings, KRW 9 million)
  → Additional KRW 3 million × 13.2–16.5% = KRW 400K–490K annual refund
  → However, major liquidity constraint (effectively no withdrawal before age 55)

3rd Priority: ISA KRW 20 million (brokerage type)
  → 9.9% separate taxation + KRW 2 million tax-exempt (low-income KRW 4 million)
  → Additional KRW 3 million tax credit possible upon transfer to pension savings at maturity

4th Priority: General brokerage account (centered on domestic stocks/ETFs)
  → Domestic stock-type capital gains tax-exempt (financial investment tax not introduced as of 2026.4)

5th Priority: General brokerage account (direct overseas investment)
  → Accept 22% capital gains tax. Use KRW 2.5 million deduction annually.
```

**Cautions**:
- Young people (20s, 30s) need liquidity → no all-in on pension accounts. Parallel general accounts too.
- Middle-aged and older (40s+) benefit from maximum pension account utilization.

## Korean-Specific Tax Issues (Execution)

### Health Insurance Dependent Status Boundaries
- KRW 20M annual income / KRW 10M financial income thresholds
- ISA and pension savings separate taxation generally excluded from dependent income calculation
- Upon disqualification: KRW 200K–600K+ monthly burden

### Capital Gains Tax Deduction Strategy
- KRW 2.5M overseas stock gains tax-exempt annually
- Replacement trading (sell and rebuy) for taxable base step-up
- Year-end loss offset against winning stocks

### ISA Maturity Pension Account Conversion
- Contribute to pension account within 60 days of ISA maturity
- Additional tax credit: 10% of conversion amount (max KRW 3M/year)

## Anti-patterns & Over-application

- **Opening ISA without calculating limits** — duplicate opening impossible, limit utilization fails
- **Early termination of pension savings** — 16.5% other income tax recaptures credited amount. If liquidity is needed, don't contribute in the first place.
- **100% stocks in IRP** — violates 70% risk asset cap, additional contribution restrictions
- **Direct overseas investment + high dividends** — double burden of dividend comprehensive taxation + capital gains tax
- **Ignoring health insurance premium** — designs exceeding KRW 20 million/year must recalculate dependent disqualification costs
- **Distorting investment around taxes** — irrational asset allocation "because of taxes". Taxes are an *auxiliary variable*, not a dominant variable.
- **Failure in KRW 20 million boundary obsession** — crossing the boundary without predicting ETF distribution accumulation

## Limitations

1. **The system changes annually** — Financial investment tax, ISA limits, pension savings credit rates all fluctuate
2. **Optimal solution varies by individual situation** — order changes based on income, assets, tax brackets, dependency status
3. **Limits of tax accountant advice** — tax consultation costs exceed benefits for small investors
4. **International tax changes** — FATCA, CRS, tax treaty changes
5. **Tax optimization induces risk-taking** — choosing ELS/derivatives to avoid high tax rates → different risks
6. **Residential linkage** — distorted without integrated view with real estate taxes (property tax, comprehensive real estate tax, capital gains tax, acquisition tax)

## What to Use with This Framework

- `bogleheads` — synergy maximized when low-cost index is operated in tax-advantaged accounts
- `fire-korean` — Korean FIRE path impossible without tax design
- `rebalancing` — tax-efficient rebalancing order
- `dollar-cost-averaging` — automatic transfer DCA in tax-advantaged accounts

## When This Framework is *Wrong*

- Problem is the return structure itself rather than taxes → return to `modern-portfolio-theory` etc. for redesign
- Assets too small (under tens of millions of won) → *savings rate itself* is the dominant variable over taxation
- Business owner/rental business complex → comprehensive tax accountant consultation essential (outside this framework)
- Real estate-centered assets → integrated tax design with `realty` skill

## Further Learning

- National Tax Service Hometax (hometax.go.kr) — official tax law and limit verification
- Korea Financial Investment Association ISA/pension savings guide (kofia.or.kr)
- National Pension Service — National Pension expected receipt inquiry
- Tax Watch, Sejong Newspaper, Joseilbo — policy change tracking
- Korean tax books: Tax Coordi *Tax Calculator*, Genesis Park *How to Use ISA/Pension*
- **Caution**: All tax decisions must be verified with tax accountants/FPs reflecting personal circumstances. This document is for educational purposes.

