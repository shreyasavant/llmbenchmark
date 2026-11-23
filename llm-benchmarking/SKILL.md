---
name: llm-benchmarking
description: Use to plan or coordinate an LLM benchmark project, from defining the measurement question through evaluation, analysis, and release. Trigger when a user is starting a benchmark, reviewing an evaluation plan, or unsure which benchmarking steps are needed.
---

# Plan an LLM Benchmark

Help the user build an evaluation that supports a clear, appropriately scoped claim. Select only the workflow steps relevant to the project and its constraints; do not treat the checklist as a fixed recipe.

## Workflow

1. **State the measurement question.** Clarify the capability or behavior being evaluated, who will use the result, and what a score should mean. Distinguish model capability from product quality, safety, or user outcomes when the setup only measures one of them.
2. **Check prior work.** Search for directly relevant benchmarks, datasets, and evaluation protocols. Cite current primary sources when browsing is available. Record important differences and avoid claiming novelty until the comparison supports it.
3. **Specify the task.** Define inputs, expected outputs, scoring, target population, and exclusions. Identify whether results depend on tools, retrieval, context, prompting, or human judgment.
4. **Plan the data.** Track provenance, permitted uses, annotation rules, quality checks, privacy handling, and likely train/test leakage. Do not assume generated data represents real-world data without validation.
5. **Choose comparisons and metrics.** Select relevant models, baselines, conditions, and metrics. Justify choices against the task and the claims. Plan uncertainty estimates and subgroup or slice analyses where the data supports them.
6. **Pre-specify and run.** Freeze the evaluation protocol before inspecting test results where feasible. Log model identifiers and dates, prompts, decoding settings, software versions, raw outputs where permitted, and failures. Protect credentials and follow provider and dataset terms.
7. **Audit and explain.** Verify calculations and denominators, examine uncertainty and meaningful slices, look for shortcuts and failure modes, and state what the results do not establish.
8. **Report and release.** Prepare enough detail for others to understand or reproduce the evaluation. Check data and code licenses, privacy, release risks, versioning, and venue requirements before publication.

## Delegate to focused skills

Use the repository skills that match the current step: `define-benchmark-gap`, `survey-existing-benchmarks`, `scope-benchmark-task`, `curate-benchmark-data`, `build-benchmark-splits`, `design-benchmark-metrics`, `select-benchmark-baselines`, `run-benchmark-experiments`, `audit-benchmark-results`, `analyze-benchmark-errors`, `structure-benchmark-paper`, `select-benchmark-venue`, and `plan-benchmark-release`.

## Output

Return a concise plan with the measurement question, chosen steps, assumptions, decisions still needed, risks to validity, and the next concrete action. Do not invent benchmark facts, results, citations, or completed checks. Mark unknowns as unknown and distinguish proposed checks from checks actually performed.
