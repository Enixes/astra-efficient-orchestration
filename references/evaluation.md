# Evaluation

Evaluate task economics, not model vibes.

## Compare routes

Run a representative suite with fixed prompts and repository states:

- Route A: Astra `xhigh` root using this skill.
- Route B: Astra `medium` root using the same worker routing.
- Route C: single-agent Astra at the user's normal effort.

Randomize route order when practical. Blind the final output to the scorer.

## Record

- Task completion: pass, partial, fail.
- Quality: correctness, completeness, requirement adherence, maintainability.
- Rework: follow-up turns, retries, reverted edits, human corrections.
- Usage: visible allowance change or credits, worker count, model mix, large-context repetitions.
- Time: wall time and user wait time.
- Verification: meaningful checks run and failures caught.

## Decision rule

Prefer the route that preserves the required quality floor and lowers median usage or rework. Keep Astra `xhigh` as root when its better task graph and integration offset its higher per-call cost. Reduce worker count or effort before lowering the root when decomposition mistakes are the main source of waste.

Do not claim parity from one demo. Re-test on the user's actual mix of coding, research, and artifact tasks.

## Failure diagnosis

| Symptom | Likely cause | Adjustment |
|---|---|---|
| Many agents, little unique evidence | Role-based spawning | Raise delegation threshold; merge work packages |
| Workers redo repository discovery | Oversized or vague scope | Send paths, symbols, and known facts in the packet |
| Cheap worker needs repeated rescue | Model underfit | Move that subtask one tier up |
| Astra usage dominates | Too many control-point calls | Integrate once; remove routine Astra review |
| Tests dominate usage/time | Verification too broad | Run affected checks first; broaden on evidence |
| Output is polished but incomplete | Weak completion contract | Make deliverable and acceptance criteria explicit |
