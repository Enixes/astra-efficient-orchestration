---
name: astra-efficient-orchestration
description: Orchestrate complex multi-step Codex work on ChatGPT Plus or Pro for maximum quality per unit of plan usage, using GPT-6 Astra xhigh at high-judgment control points and lower-cost GPT-5.6 workers for bounded subtasks. Use when work has separable research, code, verification, or review streams, or when the user asks for cost-efficient multi-agent routing.
---

# Astra Efficient Orchestration

Use Astra for decisions that determine the whole run. Spend cheaper models on narrow execution. Optimize successful task completion per unit of plan usage, not the apparent cheapness of any single call.

The user's instructions take precedence over this skill.

## Route the run

1. Classify the task before delegating.
   - Work directly when the task is small, tightly coupled, or cheaper to complete than to explain to another agent.
   - Orchestrate when at least two bounded work packages are independent, parallel work shortens the critical path, or an independent perspective materially reduces risk.
2. When model and effort are selectable, use GPT-6 Astra at `xhigh` for the root orchestrator. Treat the user's observed efficiency gain as a working policy to evaluate, not a universal cost guarantee.
3. Choose the plan profile in [usage-profiles.md](references/usage-profiles.md). If the plan is unknown, use Plus Lean.
4. Draw the smallest useful task graph. Delegate work packages, not generic roles.
5. Choose each worker from [model-routing.md](references/model-routing.md). Use the least expensive model likely to meet the subtask's acceptance criteria in one pass.
6. Send every worker a bounded packet using [task-packets.md](references/task-packets.md). Give minimum sufficient context and an explicit stop condition.
7. While workers run, keep the root on the shared or critical path. Do not duplicate a worker's assigned investigation.
8. Integrate once, resolve conflicts, and verify only the affected behavior. Broaden checks only after a failure, a shared-system change, or an unresolved concern.
9. Escalate to an independent Astra review only when the review gate below opens.
10. Finish the requested deliverable. Do not spend remaining budget on unrequested polish.

## Delegate only positive-value work

Delegate when all of these are true:

- The objective and deliverable can be stated precisely.
- The worker can proceed without repeatedly asking the root for context.
- The likely quality or latency gain exceeds task-packet and integration overhead.
- The worker can stop after a bounded search, edit, test, or review.

Keep work at the root when any of these are true:

- It changes architecture, product intent, scope, permissions, or irreversible state.
- It requires most of the conversation or repository context.
- Multiple workers would read the same large material or edit the same files.
- The expected work is only a few tool calls or one localized change.

Do not spawn every role shown in an orchestration diagram. Subagents must not create child agents unless the root explicitly authorizes a named, bounded subtask.

## Control context and retries

- Prefer a self-contained task packet with no forked history for independent work. Include only the smallest recent history needed when user intent or prior decisions matter.
- Point to target paths, symbols, URLs, or questions. Do not ask several workers to rediscover the same scope.
- Reuse an existing idle worker for a related follow-up instead of creating a new one.
- Ask for evidence, changed paths, verification results, and blockers; omit process narration.
- Stop exploration when enough evidence exists to act.
- Repair a narrow miss with a focused follow-up. Replan only when the task graph or assumptions were wrong.
- Keep stable prompt prefixes stable when the harness supports caching or mid-conversation effort changes.

## Open the independent-review gate

Use a separate Astra `xhigh` reviewer only when at least one condition holds:

- The change is security-, privacy-, finance-, legal-, migration-, or data-loss-sensitive.
- The implementation is broad, difficult to reverse, or spans several subsystems.
- Worker conclusions conflict or important evidence remains weak.
- Tests cannot cover a consequential behavior.
- The user explicitly asks for an independent review.

Otherwise, the root performs the final review and targeted verification itself.

## Calibrate rather than assume

When optimizing this skill, compare routes on the same tasks. Track completion, quality, retries, elapsed time, worker calls, context duplication, and visible usage. Use [evaluation.md](references/evaluation.md) and [evals.json](assets/evals.json). Keep `xhigh` root orchestration only while it improves total task economics for the user's workload.

For copyable invocations, read [prompt-recipes.md](references/prompt-recipes.md). For current source assumptions and dated pricing evidence, read [research-basis.md](references/research-basis.md).
