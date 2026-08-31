<div align="center">

# Harpd

**AI Cost Intelligence for the agent era** — measure, optimize, and control what your production AI actually spends.

Website: **<https://harpd.com>**

</div>

---

## What is Harpd?

**Harpd** ([harpd.com](https://harpd.com)) is an AI Cost Intelligence platform for teams running AI agents and LLM workloads in production. It measures the metric that matters — **cost per successful task**, not per-call price — and provides the tooling to optimize model choice and control agent payments (x402 / USDC) before spend happens, not after.

## Open-source packages (@harpd/*)

All MIT-licensed, zero runtime dependencies:

| Package | Purpose |
| --- | --- |
| [`@harpd/observe`](https://github.com/harpd-dev/observe) | x402 V2 observability + budget-control SDK for agent payments — the 4 lifecycle hooks, above any Facilitator |
| [`@harpd/agent-budget-policy`](https://github.com/harpd-dev/agent-budget-policy) | Local, synchronous budget control SDK — declare caps and evaluate them before a payment is sent |
| [`@harpd/x402-logging-middleware`](https://github.com/harpd-dev/x402-logging-middleware) | Drop-in x402 payment logging middleware for Node HTTP / Express |
| [`@harpd/mcp-paid-tool-starter`](https://github.com/harpd-dev/mcp-paid-tool-starter) | Starter SDK for MCP tools that require payment before they run |
| [`@harpd/agent-transaction-audit-schema`](https://github.com/harpd-dev/agent-transaction-audit-schema) | Canonical, protocol-agnostic audit record for agent payments (x402 / MPP / AP2) |

## Benchmarks & tools

- [`llm-cost-benchmark`](https://github.com/harpd-dev/llm-cost-benchmark) — public, reproducible LLM cost benchmarks ranked by **cost per successful task** → [harpd.com/benchmarks](https://harpd.com/benchmarks/)
- [`model-replacement-benchmark`](https://github.com/harpd-dev/model-replacement-benchmark) — decide whether a cheaper model can safely replace your current one → [harpd.com/modelswitch](https://harpd.com/modelswitch/)
- [`ai-agent-cost-calculator`](https://github.com/harpd-dev/ai-agent-cost-calculator) — estimate the monthly bill of an autonomous agent making thousands of paid calls → [harpd.com/ai-agent-cost-calculator](https://harpd.com/ai-agent-cost-calculator/)
- [`cost-per-successful-task`](https://github.com/harpd-dev/cost-per-successful-task) — the metric production AI systems actually pay against → [harpd.com/cost-per-successful-task](https://harpd.com/cost-per-successful-task/)

## Products

- **[Harpd Rank](https://harpd.com/rank/)** — transparent product rankings for makers (Overall / Monthly / Weekly Top 100)
- **[ModelSwitch](https://harpd.com/modelswitch/)** — AI model cost audits and switching recommendations
- **[Spend Control](https://harpd.com/products/spend-control/)** — budgets and guardrails for agent payments
- More at **[harpd.com](https://harpd.com)**

## Contact

- Website: <https://harpd.com>
- Support: <mailto:harpdsupport@gmail.com>
- Security: [harpd.com/security](https://harpd.com/security/)
