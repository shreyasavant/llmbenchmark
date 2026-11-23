---
name: scope-benchmark-task
description: Use once the gap is defined, before any data is collected, to lock the exact task definition, input/output format, and difficulty taxonomy for an LLM benchmark. Trigger whenever the user is deciding what the benchmark will actually ask models to do, or when scope is still vague.
---

# Scope the Benchmark Task

## Purpose
Convert the gap statement into an exact, unambiguous task definition. Everything downstream (data collection, metrics, baselines) depends on this being precise now rather than retrofitted later.

## Process
1. Write the exact input schema and output schema. Not "the model answers questions" — the literal fields, types, and structure (e.g., input: {context, question}, output: {answer, evidence_span}).
2. Classify the task type explicitly: classification, generation, multi-step reasoning, agentic/tool-use, retrieval-augmented, or a mix. If it's a mix, plan to report results separately by type — don't average across task types in headline numbers.
3. Define a difficulty taxonomy now (e.g., easy/medium/hard, or by required sub-skill). This needs to exist before data collection, not after, or stratification becomes a manual relabeling pass later.
4. Write an explicit out-of-scope list: what the benchmark deliberately does not test, with a one-line reason for each exclusion.

## Output
A short task spec: schema, task taxonomy, difficulty levels with example criteria for each, out-of-scope list.

## Pitfalls
- Vague schemas lead to inconsistent annotation later — nail down types and structure now.
- Skipping the out-of-scope list invites "why didn't you test X" reviews; stating it preempts that.
