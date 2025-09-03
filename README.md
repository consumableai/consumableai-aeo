# consumableai-aeo

[![PyPI version](https://badge.fury.io/py/consumableai-aeo.svg)](https://pypi.org/project/consumableai-aeo/)
[![PyPI downloads](https://img.shields.io/pypi/dm/consumableai-aeo.svg)](https://pypi.org/project/consumableai-aeo/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**AEO/GEO** (Answer Engine Optimization / Generative Engine Optimization) helper for quick audits and lightweight keyword discovery.

- `audit <url>`: Inspect basic **AEO/GEO** signals — title, description, robots, canonical, JSON-LD types, OG/Twitter tags, headings, readability proxy.
- `keywords <url|path>`: Extract candidate phrases from page text (RAKE-like) for **AI SEO analysis**.
- `competitors <url1> <url2> ...`: Aggregate and compare **competitor keywords** across multiple URLs.

> Built by [Consumable AI](https://www.consumableai.com) — tools for **AI SEO analyser**, **AEO**, **GEO**, **organic growth**, **marketing intelligence**, and **CAC reduction**.

git s**📦 Available on [PyPI](https://pypi.org/project/consumableai-aeo/)**

---

## Install

```bash
pip install consumableai-aeo
```

## CLI Usage

```bash
consumableai-aeo audit https://www.consumableai.com --json
consumableai-aeo keywords https://www.consumableai.com --top 25
consumableai-aeo competitors https://site-a.com/page https://site-b.com/page --top 20 --json
```

## Python API

```python
from consumableai_aeo import audit_url, keywords_from_url, competitor_keywords

report = audit_url("https://www.consumableai.com")
phrases = keywords_from_url("https://www.consumableai.com", top_n=25)
comp = competitor_keywords(["https://a.com", "https://b.com"], top_n=20)
```

## Checks
- Title & description presence and helpful ranges
- Canonical, robots meta (`index/follow`), OG/Twitter tags
- JSON-LD presence and detected `@type` (Product, Article, FAQPage…)
- H1/H2 counts and uniqueness of H1
- Image `alt` coverage
- Readability proxy (Flesch reading ease)
- AEO/GEO score (0–100) with per-signal breakdown

> This is a **lightweight heuristic** — great for quick checks and CI guards. For deeper analysis and automated fixes, visit [Consumable AI](https://www.consumableai.com).
