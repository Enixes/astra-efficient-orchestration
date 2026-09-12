# Research basis

Checked 2026-09-12. Recheck current plan and model documentation before relying on exact limits or rates.

## Official guidance used

- [GPT-6 Astra model guidance](https://developers.openai.com/api/docs/guides/latest-model?model=gpt-6-astra) says Astra is strong on multistep work, can use fewer output tokens per task than earlier models, supports multi-agent orchestration, is sensitive to skills and `AGENTS.md`, may delegate less unless prompted, and can over-test small coding changes.
- [Rethinking skills and prompts for GPT-6 Astra](https://developers.openai.com/blog/rethinking-skills-and-prompts-for-gpt-6-astra) recommends short skill descriptions, progressive disclosure, and auditing overlapping instructions rather than loading large skill stacks.
- [ChatGPT pricing](https://learn.chatgpt.com/docs/pricing) says Plus and Pro share usage across ChatGPT Work and Codex; usage depends on model, context, reasoning, tools, retrieval, and caching. It recommends precise prompts, limited source material, smaller `AGENTS.md`, fewer MCP servers, and smaller models for routine work.

## Dated cost signal

The 2026-09-12 credit table lists per-million-token rates of Astra 250 input / 25 cached / 1250 output; Sol 100 / 10 / 500; Terra 50 / 5 / 300; and Luna 5 / 0.5 / 30. This supports a tiered router, but exact rates are not embedded in the runtime rules because they can change.

## User evidence incorporated

The user's supplied agent-tree diagram proposed an Astra root, Luna exploration and research, Sol implementation, Astra integration, and conditional Astra review. The user also reported that Astra `xhigh` as root produced better output and usage than lower-effort orchestration in their testing.

This skill adopts `xhigh` as the root policy and changes the original tree in three ways:

1. It adds Terra for routine production work between Luna and Sol.
2. It uses soft plan-specific concurrency ceilings.
3. It makes independent Astra review conditional rather than automatic.

The resulting claim is a testable hypothesis: better root decisions can reduce total retries and context duplication enough to offset the root's higher effort. The evaluation suite is required before claiming parity for a specific workload.
