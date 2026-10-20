# QuantCordis —— 文档索引

[English](README.md) | **中文**

## 语言约定

```
docs/ 下的文档以中文撰写 —— 它们是这个项目的工作笔记，不是打磨过的手册。
对英文读者做了两件事：

1. 本索引给每篇文档一句英文概括，便于找到需要的那一篇。
2. 2026-10-20 之后新增的小节，开头都带一段 "EN summary" 英文摘要。

完整英译是一个已知缺口，不是已完成的功能。
```

## 一、数据地基

| 文档 | 它回答什么 | 行数 |
|---|---|---|
| [PRICE-CONVENTIONS.md](PRICE-CONVENTIONS.md) | `none` / `front` / `back` 三种价格实测是什么；以及 `front_ratio` / `back_ratio` 为什么不是名字暗示的东西 | 208 |
| [DATA-LAYER-DESIGN.md](DATA-LAYER-DESIGN.md) | 实测立住的表结构：存不复权价 + 复权因子，复权本地算 | 110 |
| [ADJUST-FORMULA.md](ADJUST-FORMULA.md) | 复权公式：已确认的部分与仍未解决的线索 | 105 |
| [PRICE-GAPS-FIXED.md](PRICE-GAPS-FIXED.md) | 量级断裂核查：有多少断裂、怎么根治的 | 77 |

## 二、回测与判据

| 文档 | 它回答什么 | 行数 |
|---|---|---|
| [BACKTEST-DESIGN.md](BACKTEST-DESIGN.md) | 为什么回测器自己写而不 import，以及它拒绝做什么 | 99 |
| [STRATEGY-SCREEN.md](STRATEGY-SCREEN.md) | 六个策略在全可交易样本上、三条判据同时成立的筛选 | 333 |
| [SLIPPAGE-SENSITIVITY.md](SLIPPAGE-SENSITIVITY.md) | 唯一平均超额为正的策略，为什么扛不住滑点 | 62 |
| [SCAN-NEW-DATA.md](SCAN-NEW-DATA.md) | 用新数据层重跑的最终判据 | 147 |

## 三、因子与策略

| 文档 | 它回答什么 | 行数 |
|---|---|---|
| [CROSS-SECTION-TEST.md](CROSS-SECTION-TEST.md) | 全市场横截面因子检验 —— 第一个正面结果 | 90 |
| [FACTOR-STUDY.md](FACTOR-STUDY.md) | 可复现的因子研究 —— 以及一次结论翻转 | 85 |
| [NEUTRAL-TEST.md](NEUTRAL-TEST.md) | `ep` 通过市值中性化检验，但样本外衰减严重 | 83 |
| [OOS-TEST.md](OOS-TEST.md) | 样本外检验：`ep` 衰减严重，最近两年为负 | 95 |
| [STYLE-VS-ARBITRAGE.md](STYLE-VS-ARBITRAGE.md) | `ep` 为什么失效：不是风格切换，是被套利掉了 | 88 |
| [FUNDAMENTAL-TEST.md](FUNDAMENTAL-TEST.md) | 基本面家族也不是新家族 | 105 |
| [PORTFOLIO-TEST.md](PORTFOLIO-TEST.md) | 多策略组合无用 —— 它们是同一个信号 | 73 |
| [LIMIT-UP-TEST.md](LIMIT-UP-TEST.md) | A 股独有现象的第一个测试：首板策略 | 85 |
| [SENTIMENT-TIMING.md](SENTIMENT-TIMING.md) | 市场情绪择时：信号存在，但口径不可交易 | 391 |

## 四、决策与约定

| 文档 | 它回答什么 | 行数 |
|---|---|---|
| [DECISIONS.md](DECISIONS.md) | 设计决策，以及每条的理由 | 21 |
| [ROADMAP.md](ROADMAP.md) | 按组件决定复用还是自建 | 68 |
| [SERVICE-CONVENTION.md](SERVICE-CONVENTION.md) | 端口与接口约定 | 41 |

## 五、研究纪律

| 文档 | 它回答什么 | 行数 |
|---|---|---|
| [RESEARCH-METHOD.md](RESEARCH-METHOD.md) | 规矩清单。每条都来自一次具体的错；写不出案例的规矩不收 | 746 |

## 六、对标与评估

| 文档 | 它回答什么 | 行数 |
|---|---|---|
| [MARKET-LANDSCAPE.md](MARKET-LANDSCAPE.md) | A 股量化全景，以及本项目对标什么 | 165 |
| [OPEN-SOURCE-STACK.md](OPEN-SOURCE-STACK.md) | 可复用的 MIT / Apache 栈，核实过而不是假设 | 98 |
| [VNPY-ASSESSMENT.md](VNPY-ASSESSMENT.md) | 读源码评估 VeighNa（vn.py） | 130 |

## 先读哪篇

```
想知道数据可不可信?      → PRICE-CONVENTIONS.md，然后 DATA-LAYER-DESIGN.md
想知道策略有没有超额?    → STRATEGY-SCREEN.md，然后 SLIPPAGE-SENSITIVITY.md
想知道结论怎么被管住?    → RESEARCH-METHOD.md
想知道哪些复用哪些自建?  → ROADMAP.md
```
