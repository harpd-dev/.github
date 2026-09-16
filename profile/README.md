<div align="center">

# Harpd

**Open AI product data, rankings, benchmarks and research.**

Harpd publishes open AI product data, benchmarks, research and
machine-readable datasets — so any number it publishes can be verified, reused
and cited.

Website: **<https://harpd.com>**

</div>

---

## What is Harpd?

**Harpd** ([harpd.com](https://harpd.com)) is an independent product discovery
and ranking intelligence platform for AI tools and software. It publishes
rankings, comparisons, research, datasets, benchmarks and evidence — all under
CC BY 4.0 with a public methodology.

Harpd is not a static directory. [Harpd Rank](https://harpd.com/rank/) is a live
public leaderboard: products enter free, and optional **Rank Points are
transparent promotional placement bought with Credits** — disclosed as such,
never presented as an editorial quality score.

---

## DATA

The open data layer. Every dataset is CC BY 4.0, versioned, and served as raw
JSON + CSV from GitHub — no API key, no scraping.

| Repository | What it is |
| --- | --- |
| [`harpd-ai-datasets`](https://github.com/harpd-dev/harpd-ai-datasets) | **The main dataset.** Products, rankings (overall/monthly/weekly), categories, AI agent / AI tools / developer-tools indices, research index and the evidence graph. 11 datasets, ~7,500 records, daily sync. |
| [`harpd-rank-dataset`](https://github.com/harpd-dev/harpd-rank-dataset) | AI products and their Harpd Rank positions — frozen monthly snapshots with SHA-256 checksums. |
| [`harpd-discovery-dataset`](https://github.com/harpd-dev/harpd-discovery-dataset) | 8,600+ software / AI / developer products found on public launch & directory boards. A **coverage index, not a ranking.** |

- **Canonical source:** [harpd.com/data/](https://harpd.com/data/)
- **Methodology:** [harpd.com/rank/methodology/](https://harpd.com/rank/methodology/)
- **Licence:** CC BY 4.0 — attribution required, no endorsement implied.

## RESEARCH

Reproducible research computed from the open datasets. Every figure is derived
by code from a real dataset — nothing is authored by hand.

- [`harpd-ai-research-notebooks`](https://github.com/harpd-dev/harpd-ai-research-notebooks) — 7 Jupyter notebooks (market overview, ranking trends, agent market, developer tools, AI tools landscape, model replacement, cost per successful task) plus generated monthly reports with methodology, limitations and citations.

## BENCHMARKS

Public, reproducible benchmarks measured by **cost per successful task**, not
per-call price.

- [`llm-cost-benchmark`](https://github.com/harpd-dev/llm-cost-benchmark) — LLM cost benchmarks → [harpd.com/benchmarks](https://harpd.com/benchmarks/)
- [`model-replacement-benchmark`](https://github.com/harpd-dev/model-replacement-benchmark) — can a cheaper model safely replace yours? → [harpd.com/modelswitch](https://harpd.com/modelswitch/)
- [`cost-per-successful-task`](https://github.com/harpd-dev/cost-per-successful-task) — the metric production AI systems actually pay against
- [`ai-agent-cost-calculator`](https://github.com/harpd-dev/ai-agent-cost-calculator) — estimate an autonomous agent's monthly bill

## TOOLS

Fork-and-run applications built on the open data.

- [`harpd-ai-data-explorer`](https://github.com/harpd-dev/harpd-ai-data-explorer) — search and browse the full dataset: products, rankings, categories, agents, tools, research, evidence.
- [`harpd-ai-ranking-dashboard`](https://github.com/harpd-dev/harpd-ai-ranking-dashboard) — ranking dashboard with provenance on every chart, embeddable iframes and JSON/CSV export.

## AGENT INFRASTRUCTURE

Let AI agents and agent-payment systems query Harpd data directly.

- [`harpd-mcp`](https://github.com/harpd-dev/harpd-mcp) — **MCP server** exposing Harpd datasets to AI agents, with mandatory provenance on every result.
- [`agent-transaction-audit-schema`](https://github.com/harpd-dev/agent-transaction-audit-schema) — canonical, protocol-agnostic audit record for agent payments (x402 / MPP / AP2).

### SDK packages (`@harpd/*` on npm)

All MIT-licensed, zero runtime dependencies.

| Package | Purpose |
| --- | --- |
| [`@harpd/observe`](https://github.com/harpd-dev/observe) | x402 V2 observability + budget control for agent payments |
| [`@harpd/agent-budget-policy`](https://github.com/harpd-dev/agent-budget-policy) | Local, synchronous budget control — evaluate caps before a payment is sent |
| [`@harpd/agent-market`](https://github.com/harpd-dev/agent-market) | Turn any Hono/Node API into an x402 pay-per-call agent market |
| [`@harpd/mcp-paid-tool-starter`](https://github.com/harpd-dev/mcp-paid-tool-starter) | Build MCP tools that require payment before they run |
| [`@harpd/x402-logging-middleware`](https://github.com/harpd-dev/x402-logging-middleware) | Drop-in x402 payment logging for Node HTTP / Express |

Same SDKs in other languages: [`observe-py`](https://github.com/harpd-dev/observe-py) (Python) · [`agent-budget-policy-go`](https://github.com/harpd-dev/agent-budget-policy-go) (Go)

### Runnable examples

Clone and run — no keys, no wallet, no chain.

- [`example-agent`](https://github.com/harpd-dev/example-agent) — a paying agent using the full SDK family against a mock x402 seller
- [`mcp-paid-tool-example`](https://github.com/harpd-dev/mcp-paid-tool-example) — MCP server with one free tool and one $0.01 paid tool
- [`x402-worker-starter`](https://github.com/harpd-dev/x402-worker-starter) — Cloudflare Worker template for an x402 pay-per-call API

---

## Using Harpd data

```bash
curl -L https://raw.githubusercontent.com/harpd-dev/harpd-ai-datasets/main/data/manifest.json
```

```python
import pandas as pd
df = pd.read_json(
    "https://raw.githubusercontent.com/harpd-dev/harpd-ai-datasets/main/data/products/products.json"
)
```

Full examples (Python, JavaScript, DuckDB, SQL, pandas) live in
[`harpd-ai-datasets/examples`](https://github.com/harpd-dev/harpd-ai-datasets/tree/main/examples),
and fork-and-run starter apps in
[`templates`](https://github.com/harpd-dev/harpd-ai-datasets/tree/main/templates).

**Attribution (required by CC BY 4.0):**

```
Data from Harpd (https://harpd.com/)
```

If your project uses Harpd data, you are listed in
[adoption.md](https://github.com/harpd-dev/harpd-ai-datasets/blob/main/docs/adoption.md)
— real usage only, never estimated.

---

## Principles

Harpd does not buy stars, exchange stars, fake contributors, spam forums, or
fabricate citations. Rank Points are promotional placement and are never
described as editorial quality. Every published figure carries a timestamp, a
dataset and a methodology.

---

Website · [Data](https://harpd.com/data/) · [Research](https://harpd.com/research/) · [Rank](https://harpd.com/rank/) · [API](https://harpd.com/data/) · [GitHub](https://github.com/harpd-dev)

## Contact

- Website: <https://harpd.com>
- Support: <mailto:harpdsupport@gmail.com>
- Security: [harpd.com/security](https://harpd.com/security/)
