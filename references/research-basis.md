# Research basis

Updated 2026-09-13. Exact model availability, effort labels, pricing, and ChatGPT plan allowances may change.

## User-provided experiment

[“The Idiot Boss approach to getting more Astra/Fable quota”](https://x.com/anshuc/article/2098811738674147520) is the attached article. It compares direct Astra, Astra planning with Luna-heavy implementation, and a Luna coordinator with a single Astra implementation worker on a room-planning studio and a 3D robot scene. The author reports that delegating most implementation to Luna lowered visual quality and raised API-equivalent cost, while using Luna to coordinate and browser-test a continuing Astra worker preserved much of the visual quality at less than half the estimated cost and roughly 30% less time in those examples.

The article explicitly says OpenAI and Anthropic do not disclose a direct quota conversion. Its API-cost-as-quota assumption is a proxy, not established plan accounting. The two visual tasks are not evidence of general correctness or output parity. The author also recommends direct strong-model work when quality is paramount, strong-model planning for ambitious tasks, and a more capable coordinator when the product is hard to test.

## Other context

- [OpenAI's Astra skill/prompt guidance](https://developers.openai.com/blog/rethinking-skills-and-prompts-for-gpt-6-astra) recommends short activation descriptions, progressive disclosure, and avoiding overprescriptive instructions.
- The user previously reported better output and usage with Astra `xhigh` as an orchestrator. This skill retains that as a workload-specific option rather than overriding it with the article's visual-task route.
- The user's earlier agent-tree diagram remains a possible plan for separable work, but its Luna/Sol implementation preference should not automatically govern a coherent, quality-critical frontend.

Evaluate comparable tasks and actual visible usage before making a general claim about Plus or Pro.
