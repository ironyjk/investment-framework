# Investment Framework

**한국어** 버전은 [README.ko.md](README.ko.md)를 참조하세요.

[한국어](README.ko.md) | **English**

---

A meta-router + framework collection for personal investment decision-making. Bundles 12 frameworks — portfolio theory, systematic discipline, behavioral biases, Korean tax optimization, and FIRE — under a single routing layer.

## Design Principles

1. **No theory copy-paste, translated to Korean context** — Western frameworks (Markowitz, Bogle, Dalio, Taleb) re-applied on top of Korean institutions: jeonse (전세), ISA, pension savings accounts (연금저축), and health insurance premium implications (건보료).
2. **Not a stock picker** — No recommendations for specific tickers or funds. Only *decision structure*.
3. **Anti-pattern warnings required** — Every framework documents its downsides, limits, and failure conditions at equal weight.
4. **Behavioral bias as baseline** — A strategy you can stick to beats an optimal one. Kelly and MPT are mathematically correct but meaningless if you panic-sell.

## Structure

```
investment-framework/
├── SKILL.md                     # Meta-router — situation → framework selection
├── modern-portfolio-theory/     # Markowitz, diversification math
├── all-weather/                 # Ray Dalio, economic seasons risk parity
├── bogleheads/                  # Bogle, 3-fund low-cost index
├── barbell-strategy/            # Taleb, safe + extreme-risk poles
├── value-investing/             # Graham/Buffett, intrinsic value & margin of safety
├── factor-investing/            # Fama-French, factor premiums
├── dollar-cost-averaging/       # Fixed-amount periodic buying
├── rebalancing/                 # Periodic & band rebalancing
├── behavioral-biases/           # Kahneman/Thaler, bias countermeasures
├── kelly-criterion/             # Optimal bet sizing
├── korean-tax-optimization/     # ISA · pension · IRP · capital gains · dividend tax
└── fire-korean/                 # Korean-context FIRE path
```

## Usage

```
/money <situation description>
```

The meta-router maps signals and selects 1–3 frameworks, then executes and synthesizes via the Skill tool.

> 💡 **Short name**: after [wrapper setup](https://github.com/ironyjk/claude-frameworks-marketplace#short-command-setup-optional), callable as `/money`

## Out of Scope

- Individual stock / fund recommendations
- Market forecasts (when will it go up?)
- Short-term trading signals
- Real estate (→ [`realty`](https://github.com/ironyjk/real-estate-framework))
- Business strategy (→ `think`)
- Psychological / emotional counseling (→ `counsel`)

## Sister Repo

For situations that require evaluating real estate + financial assets together from an asset-allocation perspective (e.g., "I have 500M KRW in cash — buy a home or load up on ETFs?"), pair this with [`real-estate-framework`](https://github.com/ironyjk/real-estate-framework) (`/realty`).

## Meta

- `last_verified: 2026-04-17`
- `valid_until: 2026-10-17` — Korean tax rules (ISA, pension, financial investment tax, dividend tax) and health insurance premium calculations require re-verification within 6 months.

## Disclaimer

**This repo is a decision-support tool, not investment advice.**

- No specific stock, ETF, fund, sector, weighting, or timing recommendations are made. All buy/sell decisions are entirely the user's responsibility.
- This repo does not engage in activities classified as "유사투자자문업" (unlicensed investment advisory) under Korean capital markets law — i.e., providing specific tickers, portfolios, or signals to an unspecified audience. Only thinking structures and frameworks are provided.
- Korean tax content is current as of 2026-04-17 and may change. Consult a tax accountant or private banker for actual tax decisions.
- Past returns and cycles do not guarantee future results.
- All frameworks here are *models that can be wrong*. If reality diverges from the model, reality wins.

## Attribution & Trademarks

This project implements well-known investment frameworks for educational purposes. The following are acknowledged:

- **Bogleheads®** is a registered trademark of the John C. Bogle Center for Financial Literacy (bogleheads.org). Inspired by the philosophy of John C. Bogle, founder of Vanguard.
- **All Weather Portfolio** concept by Ray Dalio, Bridgewater Associates.

All other framework names reference published academic works and are used descriptively.

This project is not affiliated with, endorsed by, or sponsored by any of the above trademark holders.

## License

CC-BY-NC-4.0 — see [LICENSE](LICENSE) for details. Commercial licensing: ironyjk@gmail.com
