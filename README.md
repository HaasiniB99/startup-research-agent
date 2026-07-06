# Startup Research Agent

A [Claude Code](https://claude.com/claude-code) agent that runs structured, beginner-friendly startup research — for someone starting from zero business knowledge. Its behavior is defined entirely by [`CLAUDE.md`](CLAUDE.md), which Claude Code reads automatically when working in this repository.

The agent's job is to move you along a clear path: from understanding basic business concepts, to surveying industry sectors, to analyzing specific markets, to identifying real startup opportunities (gaps), and finally to understanding the financial and business terms needed to act.

Every output is meant to be based on **real, verifiable information**. Factual accuracy and practical usefulness matter more than volume or polish.

## The five-stage workflow

The research follows five stages, worked through in order, one at a time:

1. **Foundations** — core concepts a beginner needs first (what a startup is vs. a small business/company/LLP/private limited, business models, product vs. service, B2B/B2C/D2C, revenue/profit/market, etc.).
2. **Sector Survey** — a broad map of major industry sectors (fintech, healthcare, agritech, edtech, retail/e-commerce, and more): what each does and how it makes money, to help you discover what interests you.
3. **Sector Deep-Dive** — for a chosen sector: sub-fields and specific markets, how they function, the main players, typical business models, and known pain points (with India-vs-global differences where relevant).
4. **Opportunity & Gap Analysis** — real gaps and unmet needs, existing competitors, how a new entrant could differ, the risks, and an honest view of cost, revenue, and profitability.
5. **Business & Finance Vocabulary** — the terms you need to operate (CAC, LTV, EBITDA, margins, burn rate, runway, MRR/ARR, unit economics, TAM/SAM/SOM, valuation, equity, funding stages, and more), each with a plain-language definition and why it matters.

> Stages 3 and 4 are handled together by a dedicated sub-agent defined in [`.claude/agents/sector-deep-dive.md`](.claude/agents/sector-deep-dive.md).

## Repository structure

```
CLAUDE.md                 # Agent instructions (Claude Code loads this automatically)
foundations/              # Stage 1 — concept explanations
sectors/                  # Stage 2 sector survey + per-sector deep-dives (Stages 3 & 4)
glossary/                 # Stage 5 — business & finance vocabulary
.claude/agents/           # The sector-deep-dive sub-agent definition
```

## How to use it

1. Install [Claude Code](https://claude.com/claude-code).
2. Clone this repository and open Claude Code in the project directory:
   ```bash
   git clone https://github.com/<your-username>/startup-research-agent.git
   cd startup-research-agent
   claude
   ```
3. Claude Code reads `CLAUDE.md` automatically. Tell it which stage you want to work on (e.g. *"Let's start Stage 1"* or *"Deep-dive the fintech sector"*), and it will research and explain step by step.

## Principles the agent follows

- **No fabricated facts** — no invented statistics, market sizes, company names, or funding figures. Unverifiable claims are flagged as needing verification.
- **Beginner-first** — plain English, every business/finance term defined the first time it appears.
- **India-aware** — it never assumes India and other countries behave the same; it states which one a claim applies to.
- **Honest about uncertainty** — it separates established facts from general reasoning from unverified claims.

## License

Copyright © 2026 HaasiniB99.

This work is licensed under the **[Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/)** license — see [`LICENSE`](LICENSE) for the full text. You may share and adapt the material with attribution, but **not for commercial purposes**.

## Note

This is a research and learning workspace. The content is educational and reflects research at the time it was written — verify specific figures independently before acting on them. It is not financial, legal, or investment advice.
