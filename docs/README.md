# QuantCordis — documentation index

**English** | [中文](README.zh-CN.md)

## Language policy

```
The documents under docs/ are written in Chinese — they are the working notes of this project,
not a polished manual. Two accommodations are made for English readers:

1. This index gives every document an English one-liner, so you can find the one you need.
2. Sections added from 2026-10-20 onward carry an inline "EN summary" block at the top.

Full English translations are a known gap, not a finished feature.
```

## 1. Data foundation

| Document | What it answers | Lines |
|---|---|---|
| [PRICE-CONVENTIONS.md](PRICE-CONVENTIONS.md) | What `none` / `front` / `back` prices actually are, measured — and why `front_ratio` / `back_ratio` are not what their names suggest | 208 |
| [DATA-LAYER-DESIGN.md](DATA-LAYER-DESIGN.md) | The schema that survived measurement: raw prices + adjustment factors, computed locally | 110 |
| [ADJUST-FORMULA.md](ADJUST-FORMULA.md) | The adjustment formula — what is confirmed, and which clues are still open | 105 |
| [PRICE-GAPS-FIXED.md](PRICE-GAPS-FIXED.md) | Magnitude-break audit — how many breaks existed and how they were rooted out | 77 |

## 2. Backtest and criteria

| Document | What it answers | Lines |
|---|---|---|
| [BACKTEST-DESIGN.md](BACKTEST-DESIGN.md) | Why the backtester is written here instead of imported, and what it refuses to do | 99 |
| [STRATEGY-SCREEN.md](STRATEGY-SCREEN.md) | Six strategies over the full tradable sample under three simultaneous criteria | 333 |
| [SLIPPAGE-SENSITIVITY.md](SLIPPAGE-SENSITIVITY.md) | The one strategy with positive mean excess — and why slippage removes it | 62 |
| [SCAN-NEW-DATA.md](SCAN-NEW-DATA.md) | The final criteria re-run on the new data layer | 147 |

## 3. Factors and strategies

| Document | What it answers | Lines |
|---|---|---|
| [CROSS-SECTION-TEST.md](CROSS-SECTION-TEST.md) | Full-market cross-sectional factor test — the first positive result | 90 |
| [FACTOR-STUDY.md](FACTOR-STUDY.md) | Reproducible factor study — including one conclusion that flipped | 85 |
| [NEUTRAL-TEST.md](NEUTRAL-TEST.md) | The `ep` factor survives market-cap neutralization, but only barely and not out of sample | 83 |
| [OOS-TEST.md](OOS-TEST.md) | Out-of-sample test: `ep` decays hard, negative in the last two years | 95 |
| [STYLE-VS-ARBITRAGE.md](STYLE-VS-ARBITRAGE.md) | Why `ep` stopped working: it was arbitraged away, not a style rotation | 88 |
| [FUNDAMENTAL-TEST.md](FUNDAMENTAL-TEST.md) | The fundamental family is not a new family either | 105 |
| [PORTFOLIO-TEST.md](PORTFOLIO-TEST.md) | Combining strategies does not diversify — they are the same signal | 73 |
| [LIMIT-UP-TEST.md](LIMIT-UP-TEST.md) | The first A-share-specific test: limit-up (first board) strategy | 85 |
| [SENTIMENT-TIMING.md](SENTIMENT-TIMING.md) | Market sentiment timing: the signal exists, but not in a tradable form | 391 |

## 4. Decisions and conventions

| Document | What it answers | Lines |
|---|---|---|
| [DECISIONS.md](DECISIONS.md) | The design decisions, with the reason each was taken | 21 |
| [ROADMAP.md](ROADMAP.md) | Which components are reused and which are rewritten, per component | 68 |
| [SERVICE-CONVENTION.md](SERVICE-CONVENTION.md) | Port and interface conventions | 41 |

## 5. Research discipline

| Document | What it answers | Lines |
|---|---|---|
| [RESEARCH-METHOD.md](RESEARCH-METHOD.md) | The rule list. Every rule comes from a concrete mistake; a rule without a case does not get in | 746 |

## 6. Comparison and assessment

| Document | What it answers | Lines |
|---|---|---|
| [MARKET-LANDSCAPE.md](MARKET-LANDSCAPE.md) | The A-share quant landscape, and what this project is benchmarked against | 165 |
| [OPEN-SOURCE-STACK.md](OPEN-SOURCE-STACK.md) | The reusable MIT / Apache stack, verified rather than assumed | 98 |
| [VNPY-ASSESSMENT.md](VNPY-ASSESSMENT.md) | VeighNa (vn.py) assessed by reading its source | 130 |

## Which document should I read first?

```
Want to know whether the data can be trusted?   → PRICE-CONVENTIONS.md, then DATA-LAYER-DESIGN.md
Want to know whether a strategy has an edge?    → STRATEGY-SCREEN.md, then SLIPPAGE-SENSITIVITY.md
Want to know how conclusions are policed here?  → RESEARCH-METHOD.md
Want to know what is and is not reused?         → ROADMAP.md
```
