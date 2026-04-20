---
name: money-router-prompt
version: "1.0.0"
description: "LLM-as-Router prompt template for selecting the optimal personal investment framework given a situation. Replaces keyword-matching Detection Matrix."
type: router_prompt
target_repo: investment-framework
---

# Money Router — LLM Selection Prompt

This file is consumed by `pag_pipeline.py::route(repo="investment", question, router_llm)`.
It lists every framework in this repo with a one-line "when to use" description and a concrete example scenario. The router LLM is asked to return **exactly one framework name**.

---

## System Prompt

```
You are an investment strategist acting as a framework selector.
Given a situation, pick the SINGLE framework that best fits.

Output ONLY the framework name (lowercase, exactly as listed below). No explanation, no punctuation, no quotes.

If the situation is ambiguous, prefer the framework whose Example most closely matches the scenario's CORE problem, not just surface keywords.
```

---

## Framework Catalog

Each entry: `name` — **when to use** (one line) / **example** (one concrete scenario).

### Portfolio Construction (allocation & diversification)

**modern-portfolio-theory** — Question is about constructing overall portfolio weights using risk, return, and correlation (Efficient Frontier).
Example: "I have 200M KRW to allocate across stocks, bonds, and gold. What weights minimize volatility for my expected return target?"

**all-weather** — Want a portfolio that survives across growth/inflation regimes without predicting which one is coming (Dalio style).
Example: "I'm worried about both recession and inflation. Build me an allocation that won't blow up in either regime, even if returns are moderate."

**bogleheads** — Beginner needs a complete investing philosophy/starter playbook (where to begin, what accounts, what funds, monthly contribution plan); the default "how do I invest?" answer for anyone without a pre-existing strategy.
Example: "I have about $2,000 per month in spare funds and want to start investing but don't know where to begin." (beginner asking for a complete starting framework)

**barbell-strategy** — Worried about tail risk and black swans; want 85-90% ultra-safe + 10-15% convex upside, nothing in the middle.
Example: "I can't stand the idea of losing everything in a crash, but I still want asymmetric upside. Design 90% T-bills + 10% venture bets."

### Stock Selection & Sizing (which assets, how much)

**value-investing** — Interested in picking individual undervalued stocks based on intrinsic value and margin of safety (Graham/Buffett).
Example: "This Korean industrial stock trades at 0.6x book value. Walk me through whether it's a margin-of-safety buy or a value trap."

**factor-investing** — Want exposure to systematic return premia (value, size, momentum, quality) via smart-beta or factor ETFs.
Example: "Why do MSCI offer 12 different indices for the same region? Which factor tilts make sense for my 30-year accumulation horizon?"

**kelly-criterion** — Need to decide position size or leverage ratio given an edge and its odds; bet sizing is the core question.
Example: "My auto-trading bot has a 55% win rate with 1.2:1 payoff. What fraction of capital per trade, and why is full Kelly a bad idea?"

### Behavior & Execution (when and how to act)

**dollar-cost-averaging** — Specifically debating LUMP-SUM vs PHASED entry for an existing pile of cash (bonus, severance, inheritance); the core question is "all at once or spread over N months". NOT for beginners asking how to invest monthly income (→ `bogleheads`).
Example: "I just received a 300M KRW severance. Should I invest it all next Monday, or spread it across 12 months to reduce entry-timing regret?"

**rebalancing** — Portfolio weights have drifted from target allocation; need rules for when and how to restore them (calendar vs threshold).
Example: "My stocks ran up and are now 75% of the portfolio instead of 60%. Do I rebalance on a date, on a drift threshold, or leave it?"

**behavioral-biases** — Core problem is the investor's own psychology — panic selling, FOMO buying, anchoring, loss aversion.
Example: "I panic-sold everything in the March 2024 drawdown and missed the recovery. How do I design pre-commitments so this doesn't happen again?"

### Korean Regime & Life Planning

**korean-tax-optimization** — Question hinges on Korean tax containers (ISA, 연금저축, IRP), dividend/capital-gains tax, or health-insurance premium impact.
Example: "I max out ISA every year. Should I also push into IRP, and how does foreign-stock capital-gains tax change my rebalancing decisions?"

**fire-korean** — Question is about retiring early in the Korean context — 4% rule adapted, National Pension, real estate, withdrawal phase.
Example: "I'm 42, have 1.5B KRW + paid-off apartment. When can I quit, accounting for National Pension and health insurance after retirement?"

---

## User Prompt Template

```
## Situation
{scenario}

## Task
From the catalog above, output the SINGLE framework name that best fits.

Answer (one word, lowercase):
```

---

## Routing Notes (for maintainers, not shown to LLM)

- **`modern-portfolio-theory` vs `all-weather` vs `bogleheads`**: MPT is "compute optimal weights from risk/return/correlation inputs"; All Weather is "regime-agnostic allocation, don't forecast"; Bogleheads is "index-and-forget at minimum cost". Route by the stated mental model, not by overlap in asset mix.
- **`barbell-strategy` vs `all-weather`**: Barbell is tail-risk obsession + convex upside; All Weather is smooth ride across regimes. "Don't want to lose everything" → barbell; "don't want a bad decade" → all-weather.
- **`dollar-cost-averaging` vs `kelly-criterion`**: DCA is about *timing a cash deployment*; Kelly is about *position size per bet given edge*. If the question is "when", route DCA; if "how much per trade", route Kelly.
- **`bogleheads` vs `dollar-cost-averaging` (critical)**: "I have $X/month and want to start investing" → `bogleheads` (beginner needs the full philosophy). DCA is ONLY for the specific lump-sum-vs-phased dilemma with an EXISTING pile of cash. Monthly recurring contributions from income are a Bogleheads implementation detail, not a DCA question.
- **`behavioral-biases` wins when emotion drove a mistake** — "I panic-sold", "bought on FOMO", "can't stick to plan". Even if the literal question is about rebalancing or allocation, the root cause is behavioral.
- **`korean-tax-optimization` trumps theory when after-tax return reverses the decision** — if the user mentions ISA/IRP/연금저축/health-insurance premium, route here even if the surface question is portfolio construction.
- **`fire-korean` is only for retirement-timing / decumulation** — if the user is 30s asking about allocation, prefer Bogleheads/MPT; fire-korean is for "when can I quit?" not "how do I invest?"
- **Exclusive routing**: If the situation fits multiple frameworks, the router picks ONE. Pipeline combination is handled in Layer 3 (the selected framework's SKILL.md may invoke others).
- **Not included here**: `money` itself (this IS money). Real-estate questions route to `realty` repo.

---

## Maintenance Protocol

Adding a new framework requires:
1. Add an entry to Framework Catalog above (name + when + example).
2. Choose an example that is **unambiguous** — if it could be confused with another listed framework, rewrite.
3. Run the evaluation set in `scripts/experiment/` to check no regression on existing scenarios.
