# Model routing

Choose by task risk and ease of judging the finished result. Check the models and effort levels actually available in the current environment.

| Route | Good fit | Main cost or risk |
|---|---|---|
| Direct Astra | Quality-first, coupled, small, or hard-to-test work | Strong model carries the full implementation and verification context |
| Luna `xhigh` coordinator → Astra `low` worker | Bounded visual/product build with a clear brief and browser-testable outcome | QA or handoff may be weak; repeated rounds can erase savings |
| Terra/Sol coordinator → Astra worker | Product work requiring more reliable planning or QA than Luna offers | More coordinator usage |
| Astra `xhigh` planner/root → bounded workers | Ambitious plan, architecture, integration, high-risk or hard-to-test work | Expensive root context and over-delegation can dominate |

The small coordinator is *glue and QA*, not the design or architecture authority. Keep the original product brief intact in the worker handoff. Send screenshots and observed failures, not a preselected implementation strategy. A capable worker should implement the main experience; use Luna/Terra for narrow lookup, mechanical edits, or checks only when these tasks are genuinely separable.

If the work is security-, privacy-, finance-, migration-, or data-loss-sensitive, do not use a cheap coordinator as a substitute for adequate judgment or required review. No route permits delegation contrary to user or environment instructions.

## Fallbacks

- If Astra worker delegation is unavailable, use direct Astra or the best available single agent; do not claim the delegated route ran.
- If the coordinator cannot inspect the result, choose a stronger coordinator or direct Astra.
- If an effort label is unavailable, preserve the role distinction and measure actual outcomes instead of equating labels.
- If the worker needs repeated full-context rescue, switch routes rather than persisting with a superficially cheap call.

Do not assume API token pricing maps directly to Plus/Pro usage allowances.
