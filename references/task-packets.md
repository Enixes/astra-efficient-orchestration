# Task packets

A task packet is the main defense against duplicated context and retries.

## Required fields

```text
Objective: <one bounded result>
Deliverable: <finding, patch, tests, or review>
Scope: <paths, symbols, URLs, or questions>
Context: <only facts needed to proceed>
Constraints: <permissions, style, compatibility, non-goals>
Acceptance: <observable success conditions>
Stop: <when to stop searching or editing>
Return: <evidence, changed paths, checks, blockers>
```

## Explorer or researcher

```text
Investigate only <question> in <scope>. Return the smallest evidence set that lets the root decide. Cite file paths, symbols, commands, or authoritative URLs. Stop after the question is answered or after <bounded limit>; report uncertainty instead of broadening the search. Do not edit files and do not spawn child agents.
```

## Implementation worker

```text
Implement <change> only in <scope>. Preserve <constraints>. Success means <acceptance criteria>. Run <targeted checks> if available. Stop once the criteria pass; do not add unrelated improvements. Return changed paths, test results, assumptions, and blockers. Do not spawn child agents.
```

## Independent reviewer

```text
Review the integrated result against <requirements and risk>. Look for consequential correctness, security, data-loss, compatibility, and missing-verification issues. Do not repeat style feedback or restate passing checks. Return only actionable findings with evidence, ordered by severity; say explicitly if none are found. Do not edit files unless asked.
```

## Follow-up repair

Send the original worker the failing evidence and one correction objective. Do not resend the full conversation or reopen settled requirements.
