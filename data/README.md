# `data/` — code only, no market data

[English](#english) | [中文](#中文)

---

## English

### What lives here

```
data/adjust.py     adjustment factors: pull, validate, turn factors into prices
data/bar_none.py   unadjusted bars: schema, source column, fetch timestamp
data/db.py         connection handling and schema assumptions
data/pool.py       tradable-universe construction
```

**This directory contains code. It contains no market data.** Not a single price, bar, or factor
value is committed here.

### Why: data rights are not ours to license

```
The bars, adjustment factors and trading records this project consumes come from a data vendor
(xtdata / the QMT terminal). Those terms are between you and that vendor. They are not ours,
and they do not become MIT because our code is MIT.

⇒ Redistributing vendor data inside an MIT repository would misrepresent its terms.
```

### If you want to work with this project

```
1. Obtain your own licensed data source.
2. Point the connection settings in `.env` at it (see `.env.example`).
3. Run the fetchers under `tools/` to build the tables locally.

The code is MIT: use it, modify it, ship it.
The data is yours and your vendor's: it stays outside this repository.
```

### If a sample dataset is ever added

It must be recorded here, with **source** and **terms**, before it is committed. And it must not be
data a vendor forbids redistributing. A synthetic or heavily aggregated sample is the safe option.

### License summary

```
code (this repository)        MIT — see ../LICENSE
market data                   NOT covered by MIT; not present here
third-party content           see ../NOTICE
```

---

## 中文

### 这里放什么

```
data/adjust.py     复权因子：拉取、校验、由因子算价格
data/bar_none.py   不复权行情：表结构、来源列、抓取时间
data/db.py         连接与表结构假设
data/pool.py       可交易股票池的构造
```

**这个目录里是代码，不含任何行情数据。** 没有一个价格、一根 K 线、一个因子值被提交进来。

### 为什么：数据权利不属于我们

```
本项目消费的 K 线、复权因子与成交记录来自数据供应商（xtdata / QMT 终端）。
那些条款是你与该供应商之间的，不是我们的；也不会因为我们的代码是 MIT 就变成 MIT。

⇒ 把供应商数据放进 MIT 仓库，等于给它的条款贴错标签。
```

### 想用这个项目

```
① 自己准备有授权的数据源
② 在 `.env` 里把连接配置指向它（参考 `.env.example`）
③ 跑 `tools/` 下的抓取脚本，在本地建表

代码是 MIT：随便用、改、发。
数据属于你和你的供应商：它留在本仓之外。
```

### 如果将来要加样例数据

必须在提交**之前**写进本文件：**来源**与**条款**。而且不能是供应商禁止再分发的数据。
最安全的选择是合成数据或高度聚合的统计量。

### 许可摘要

```
代码（本仓）      MIT —— 见 ../LICENSE
行情数据          不受 MIT 覆盖；本仓不含
第三方内容        见 ../NOTICE
```
