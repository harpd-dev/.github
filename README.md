<div align="center">

# Harpd

**AI product discovery and ranking intelligence** — independent rankings, research, open datasets and evidence for AI tools and software.

Website: **<https://harpd.com>**

</div>

---

## What is Harpd?

**Harpd** ([harpd.com](https://harpd.com)) is an independent product discovery and ranking
intelligence platform for AI tools and software. It publishes rankings, comparisons, research,
datasets, benchmarks and evidence — all under CC BY 4.0 with a public methodology, so any number it
publishes can be verified, reused and cited.

Harpd is not a static directory. [Harpd Rank](https://harpd.com/rank/) is a live public
leaderboard: products enter free, and optional Rank Points are **transparent promotional placement
bought with Credits** — disclosed as such, never presented as an editorial quality score.

## Harpd open data (CC BY 4.0)

Versioned public mirrors of the Harpd datasets, published so researchers, journalists, developers
and AI systems can cite a stable snapshot instead of a URL that moves.

| Dataset | What it covers |
| --- | --- |
| [`harpd-rank-dataset`](https://github.com/harpd-dev/harpd-rank-dataset) | AI products and their Harpd Rank positions — frozen monthly snapshots with SHA-256 checksums |
| [`harpd-discovery-dataset`](https://github.com/harpd-dev/harpd-discovery-dataset) | Software, AI and developer products found on public launch & directory boards — a coverage index, not a ranking |

- **Canonical source:** [harpd.com/data/](https://harpd.com/data/) — [rank.json](https://harpd.com/data/rank.json), [rank.csv](https://harpd.com/data/rank.csv)
- **Methodology:** [harpd.com/rank/methodology/](https://harpd.com/rank/methodology/)
- **Licence:** CC BY 4.0 — attribution required, no endorsement implied

## SDK packages (@harpd/* on npm)

Harpd's open-source agent-payment tooling. All MIT-licensed, zero runtime dependencies:

| Package | Purpose |
| --- | --- |
| [`@harpd/observe`](https://github.com/harpd-dev/observe) | x402 V2 observability + budget-control SDK for agent payments — the 4 lifecycle hooks, above any Facilitator |
| [`@harpd/agent-budget-policy`](https://github.com/harpd-dev/agent-budget-policy) | Local, synchronous budget control SDK — declare caps and evaluate them before a payment is sent |
| [`@harpd/agent-transaction-audit-schema`](https://github.com/harpd-dev/agent-transaction-audit-schema) | Canonical, protocol-agnostic audit record for agent payments (x402 / MPP / AP2) |
| [`@harpd/x402-logging-middleware`](https://github.com/harpd-dev/x402-logging-middleware) | Drop-in x402 payment logging middleware for Node HTTP / Express |
| [`@harpd/mcp-paid-tool-starter`](https://github.com/harpd-dev/mcp-paid-tool-starter) | Starter SDK for MCP tools that require payment before they run |
| [`@harpd/agent-market`](https://github.com/harpd-dev/agent-market) | Turn any Hono/Node API into an x402 pay-per-call agent market — free + paid tiers, discovery metadata |

## Same SDKs, other languages

- [`observe-py`](https://github.com/harpd-dev/observe-py) — the observe SDK in Python: hooks, durable event queue, local budget control
- [`agent-budget-policy-go`](https://github.com/harpd-dev/agent-budget-policy-go) — the budget policy SDK in Go, with cross-language parity on JSON fields

## Runnable examples

Clone and run — no keys, no wallet, no chain:

- [`example-agent`](https://github.com/harpd-dev/example-agent) — a paying AI agent using the full SDK family: budget policy → 402 → pay → observe → audit, against a mock x402 seller
- [`mcp-paid-tool-example`](https://github.com/harpd-dev/mcp-paid-tool-example) — an MCP server (Claude Desktop-compatible) with one free tool and one $0.01 paid tool
- [`x402-worker-starter`](https://github.com/harpd-dev/x402-worker-starter) — Cloudflare Worker template for an x402 pay-per-call API

## Benchmarks & tools

- [`llm-cost-benchmark`](https://github.com/harpd-dev/llm-cost-benchmark) — public, reproducible LLM cost benchmarks ranked by **cost per successful task** → [harpd.com/benchmarks](https://harpd.com/benchmarks/)
- [`model-replacement-benchmark`](https://github.com/harpd-dev/model-replacement-benchmark) — decide whether a cheaper model can safely replace your current one → [harpd.com/modelswitch](https://harpd.com/modelswitch/)
- [`ai-agent-cost-calculator`](https://github.com/harpd-dev/ai-agent-cost-calculator) — estimate the monthly bill of an autonomous agent making thousands of paid calls → [harpd.com/ai-agent-cost-calculator](https://harpd.com/ai-agent-cost-calculator/)
- [`cost-per-successful-task`](https://github.com/harpd-dev/cost-per-successful-task) — the metric production AI systems actually pay against → [harpd.com/cost-per-successful-task](https://harpd.com/cost-per-successful-task/)

## Products

- **[Harpd Rank](https://harpd.com/rank/)** — transparent product rankings for makers (Overall / Monthly / Weekly Top 100)
- **[Harpd Open Data](https://harpd.com/data/)** — every public dataset as JSON and CSV, no key, CC BY 4.0
- **[ModelSwitch](https://harpd.com/modelswitch/)** — AI model cost audits and switching recommendations
- More at **[harpd.com](https://harpd.com)**

## Contact

- Website: <https://harpd.com>
- Support: <mailto:harpdsupport@gmail.com>
- Security: [harpd.com/security](https://harpd.com/security/)
