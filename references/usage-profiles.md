# Usage profiles

These are routing heuristics, not promises about plan limits or model availability.

## Plus Lean

For bounded, testable implementation, consider one Astra `low` worker under a Luna `xhigh` coordinator. Keep the same worker for focused fixes, and have the coordinator browser-test and report back. If the task is small, coupled, or quality-first, use direct Astra instead. Do not open independent researchers or reviewers by default.

## Pro Balanced

Choose the same route by task shape, not simply because Pro has a larger allowance. Terra or Sol can coordinate when product QA is demanding. For ambitious work, use Astra `xhigh` to create the plan and preserve decisions; use an Astra worker for the quality-critical build and smaller models only for bounded supporting tasks.

## Emergency Conserve

Finish the requested result. Avoid speculative parallel agents, repeated broad tests, redundant screenshots, and independent review unless risk warrants them. Use a small coordinator only when it can actually evaluate the worker and is authorized to delegate. Otherwise prefer a direct, focused run.

## User-specific override

If the user's measured tasks favor Astra `xhigh` at the root, keep that profile as the default for comparable work. Test a small-coordinator route on representative tasks before changing the default. Ask about remaining quota only when it materially changes the route.
