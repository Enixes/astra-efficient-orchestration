# Evaluation

The attached article reports an experiment on two visual projects; treat it as a promising routing hypothesis, not a universal efficiency result.

## Compare on representative tasks

- A: direct Astra, at the effort normally used for that task.
- B: Astra `xhigh` root/planner with bounded workers (the user's successful baseline).
- C: Luna `xhigh` or Terra/Sol coordinator with one continuing Astra `low` implementation worker.

Use the same initial brief, assets, acceptance checks, and starting repository state. Include visual/product tasks as well as hard-to-test or multi-service tasks where route C may lose. Record the worker prompts to detect coordinator over-prescription. Blind-score finished outputs where possible.

## Record

- Completion and user-visible quality, including responsive screenshots and functioning flows.
- Correctness, regression risk, maintainability, and required test coverage.
- Coordinator/worker calls, handoff tokens, duplicated context, repair rounds, and elapsed time.
- Visible Plus/Pro usage if exposed; otherwise label API-equivalent estimates as estimates, not quota.

Prefer the lowest-usage route meeting the same quality floor. If the small coordinator produces a lower-quality build or cannot evaluate it, strengthen QA or switch to direct/Astra-led work. If repeated worker rounds erase savings, stop and replan. Keep the user's `xhigh`-root route for workloads where it wins.

Never claim output parity or a quota multiplier from one or two examples.
