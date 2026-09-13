# Task packets

A handoff should preserve the goal, not compress the coordinator's taste into prescriptive design or architecture.

## Capable implementation worker

```text
Implement the user's brief below in one continuous thread. Use the existing project constraints and attached references. Own implementation decisions and fix issues you notice. Finish when [observable acceptance]. Return changed paths and a brief summary. [State precisely which checks you own and which the coordinator will run.] Do not spawn child agents.

User brief:
[original brief, minimally edited]

Project facts:
[only relevant paths, assets, constraints]
```

For a follow-up, reuse the worker thread if its context remains useful:

```text
On the current build, [observed behavior] at [viewport/action]. Here is the latest screenshot [attachment] and [console/test evidence]. Please fix the material issue while preserving the brief. Return only the changed paths and result.
```

The coordinator exercises the deliverable, records concrete failures, captures relevant screenshots, and decides whether another round is worth its cost. Three rounds is a useful experimental ceiling for a bounded visual task, not a universal stop rule or a reason to ship a broken result.

## Bounded support worker

```text
Answer [one question] in [specific scope] with paths or authoritative evidence. Stop once the decision is supported; do not implement, broaden the search, or spawn agents.
```

Only delegate when authorization permits it. Clearly allocate essential tests and reviews; never drop them because a worker packet asks for brevity.
