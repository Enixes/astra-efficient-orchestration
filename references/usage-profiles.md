# Usage profiles

These are soft ceilings. Use fewer agents whenever fewer will complete the task well.

## Plus Lean — default when plan is unknown

- Root: GPT-6 Astra `xhigh` when selectable.
- Direct tasks: no subagents.
- Orchestrated tasks: one delegation wave, normally one worker and at most two concurrent workers.
- Follow-up: reuse a worker for one focused correction before creating another agent.
- Review: root review by default; independent Astra review only when the review gate opens.
- Verification: the narrowest meaningful check for changed behavior.

This profile protects a relatively small shared allowance by concentrating Astra usage at decomposition and integration.

## Pro Balanced

- Root: GPT-6 Astra `xhigh` when selectable.
- Direct tasks: no subagents.
- Orchestrated tasks: one delegation wave with one to three concurrent workers.
- Second wave: allowed only for a gap discovered by the first wave, not as speculative breadth.
- Review: independent Astra review for consequential or genuinely uncertain work.
- Verification: affected checks first; broaden once when shared infrastructure or failures justify it.

Pro's larger limit buys throughput, not permission to duplicate work.

## Emergency conserve

Use when the user is near a reset or explicitly asks to minimize usage.

- Finish the current deliverable before optional work.
- Use no independent review unless the change is consequential.
- Route retrieval, classification, repository mapping, and mechanical edits to Luna or Terra.
- Prefer one strong task packet over several exploratory workers.
- Avoid image generation, broad retrieval, and repeated large test suites unless required by the task.

## Choosing a profile

Ask about plan or remaining budget only if it would materially change the route. Otherwise infer from context, state the selected profile briefly, and proceed.
