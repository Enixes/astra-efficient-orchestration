# Astra Efficient Orchestration

A cost-aware Agent Skill for routing **GPT-6 Astra** and smaller Codex models on ChatGPT **Plus or Pro**. It helps you choose between direct Astra, a lightweight coordinator with an Astra implementer, and Astra-led planning for ambitious work.

The attached [“Idiot Boss” experiment](https://x.com/anshuc/article/2098811738674147520) motivates the main change: on two visual builds, a small coordinator that browser-tested one continuing Astra implementation worker was cheaper and faster *by API-equivalent estimate* than the tested alternatives, with much less quality loss than asking Luna to implement everything. This is not a verified Plus/Pro quota conversion or a general parity claim. Your own tasks may favor an Astra `xhigh` root.

## Install

```bash
npx skills@latest add Enixes/astra-efficient-orchestration
```

Or clone into `~/.codex/skills/astra-efficient-orchestration` and start a new Codex session.

## Choose a route

| Situation | Suggested route |
|---|---|
| Small, coupled, quality-first, or hard to evaluate | Direct Astra with required checks |
| Bounded visual/product build with browser-testable acceptance | Luna `xhigh` coordinator → one Astra `low` implementation worker; reuse its thread for focused repairs |
| Product QA too demanding for Luna | Terra/Sol coordinator → Astra worker |
| Ambitious multi-step architecture or consequential integration | Astra `xhigh` plans and resolves key decisions; delegate bounded execution only when useful |

Model selection and delegation depend on your Codex environment and permissions. A coordinator should pass the original brief and evidence to the capable worker, not prescribe technical design. It owns browser QA and the final handoff; essential verification remains assigned and completed.

## Quick start

For a bounded frontend build:

```text
Use $astra-efficient-orchestration with $astra-frontend-design. If delegation is permitted, let a small coordinator give one Astra worker the original brief for the complete implementation. Reuse that worker for fixes; test in the browser and send screenshots plus concrete defects. Preserve required tests and stop when acceptance passes.
```

For quality-first or hard-to-test work:

```text
Use $astra-efficient-orchestration. Work directly with Astra unless a bounded independent support task clearly helps. Complete required verification.
```

For your existing `xhigh`-root baseline:

```text
Use $astra-efficient-orchestration with Astra xhigh at planning and integration. Delegate only bounded useful work; compare quality and visible usage before changing the route.
```

See [model routing](references/model-routing.md), [usage profiles](references/usage-profiles.md), [handoff templates](references/task-packets.md), [prompt recipes](references/prompt-recipes.md), and [evaluation guidance](references/evaluation.md). [Research basis](references/research-basis.md) separates experiment findings from quota assumptions.

Pair with [Astra Frontend Design](https://github.com/Enixes/astra-frontend-design) when visible product quality is a primary deliverable.

## Attribution

- [The user-provided experiment](https://x.com/anshuc/article/2098811738674147520)
- [OpenAI: Rethinking skills and prompts for GPT-6 Astra](https://developers.openai.com/blog/rethinking-skills-and-prompts-for-gpt-6-astra)
- [Agent Skills](https://agentskills.io/)
