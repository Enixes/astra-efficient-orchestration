# Astra Efficient Orchestration

A cost-aware multi-agent orchestration skill for **GPT-6 Astra**, **OpenAI Codex**, and ChatGPT **Plus or Pro** plans.

It keeps Astra at the high-judgment control points—scoping, delegation, integration, and exceptional review—while routing bounded work to GPT-5.6 Luna, Terra, or Sol. The goal is strong end-to-end output with less duplicated context, fewer failed branches, and better use of plan limits.

## Why this skill exists

The cheapest individual model call is not always the cheapest completed task. Weak decomposition can create overlapping investigations, repeated repository reads, unnecessary tests, and expensive retries.

This skill uses GPT-6 Astra at `xhigh` as the root orchestrator when the harness allows model and effort selection. Smaller models handle work they can reliably finish in one pass. The root then integrates once and opens an independent Astra review only when the risk justifies it.

## What it provides

- Plus Lean, Pro Balanced, and Emergency Conserve usage profiles
- A practical Astra → Luna/Terra/Sol routing policy
- A delegation threshold that prevents ceremonial subagents
- Minimal-context task packets for research, implementation, and review
- Explicit stop conditions for exploration, testing, and retries
- A risk gate for independent Astra review
- Prompt recipes for coding, research, and frontend work
- An evaluation suite for comparing quality, usage, retries, and elapsed time

## Install

Using the Agent Skills installer:

```bash
npx skills@latest add Enixes/astra-efficient-orchestration
```

Or clone it directly into the Codex skills directory:

```bash
git clone https://github.com/Enixes/astra-efficient-orchestration.git \
  ~/.codex/skills/astra-efficient-orchestration
```

Start a fresh Codex session after installation so the skill catalog refreshes.

## Quick start

### Plus

```text
Use $astra-efficient-orchestration in Plus Lean mode. Complete this task with the smallest useful agent tree and preserve output quality.
```

### Pro

```text
Use $astra-efficient-orchestration in Pro Balanced mode. Keep Astra xhigh at scoping and integration, and parallelize only independent work packages.
```

### Near your usage limit

```text
Use $astra-efficient-orchestration in Emergency Conserve mode. Finish the required deliverable, minimize duplicated context and agent count, and skip optional polish.
```

## Model routing

| Work | Preferred model | Purpose |
|---|---|---|
| Scope, architecture, arbitration, integration | GPT-6 Astra `xhigh` | Spend the strongest reasoning where decisions affect the whole run |
| Focused search, extraction, inventory, repository mapping | GPT-5.6 Luna `max` | Handle bounded evidence gathering at high volume |
| Routine implementation and targeted verification | GPT-5.6 Terra `high` | Complete well-specified production work economically |
| Difficult bounded coding, debugging, or migrations | GPT-5.6 Sol `high` | Use stronger implementation reasoning without adding another Astra control point |
| Consequential independent review | GPT-6 Astra `xhigh` | Run only when security, data-loss, compatibility, or uncertainty opens the review gate |

Exact model availability and rates change. The skill preserves these roles when a named model or effort level is unavailable.

## Core principle

**Split useful work. Do not spawn every role.**

A subtask is worth delegating only when it has a precise deliverable, can proceed with limited context, and is likely to save more time or improve more quality than its coordination overhead costs.

## Evaluation

The included suite compares:

- Astra `xhigh` orchestration using this skill
- Astra `medium` with the same worker routing
- Single-agent Astra at the user's normal effort

It records completion, correctness, rework, visible usage, worker count, repeated context, time, and verification quality. The `xhigh` root policy is an evidence-backed working hypothesis, not a universal savings claim.

## Repository structure

```text
.
├── SKILL.md
├── agents/openai.yaml
├── assets/evals.json
└── references/
    ├── evaluation.md
    ├── model-routing.md
    ├── prompt-recipes.md
    ├── research-basis.md
    ├── task-packets.md
    └── usage-profiles.md
```

## Companion skill

For product-quality frontend work, pair this with [Astra Frontend Design](https://github.com/Enixes/astra-frontend-design). Astra can own product intent and visual acceptance while bounded workers handle focused implementation and evidence gathering.

## References

- [GPT-6 Astra model guidance](https://developers.openai.com/api/docs/guides/latest-model?model=gpt-6-astra)
- [Rethinking skills and prompts for GPT-6 Astra](https://developers.openai.com/blog/rethinking-skills-and-prompts-for-gpt-6-astra)
- [Agent Skills overview](https://agentskills.io/)

