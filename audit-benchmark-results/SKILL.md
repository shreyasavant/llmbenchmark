---
name: audit-benchmark-results
description: Use after an LLM benchmark run or before sharing a leaderboard, report, or paper. Trigger when checking score calculations, comparing models, interpreting uncertainty, or validating claims against evaluation evidence.
---

# Audit Benchmark Results

Check whether the reported conclusions follow from the recorded evaluation. Work from the data and protocol the user provides; do not imply that an audit was run if inputs are missing.

## Process

1. **Trace each number.** Identify the source file or run, evaluation set/version, scoring code, unit of analysis, denominator, exclusions, and aggregation. Recompute key results when raw outputs and scoring rules are available.
2. **Check comparability.** Compare model versions and dates, prompts, tools, context, decoding, retries, budget, and other conditions that could affect results. Flag differences and avoid presenting unmatched setups as a controlled comparison.
3. **Quantify uncertainty.** Use an interval or other uncertainty estimate suited to the sampling and run design. Distinguish item-level variation from run-to-run variation. Do not treat repeated samples from one model or examples from a clustered source as independent observations without justification.
4. **Inspect coverage.** Report relevant task categories and data slices when sample sizes permit. Surface missing, failed, refused, truncated, or unscorable outputs and explain how they were handled.
5. **Probe score validity.** Check whether the metric matches the intended behavior. Consider plausible shortcuts, position or length effects, evaluator sensitivity, and contamination. Run targeted ablations only when data and budget allow; otherwise describe them as untested risks.
6. **Match claims to evidence.** Separate observed results from explanations and causal claims. Note limits from benchmark scope, data provenance, model access, versions, and measurement uncertainty.
7. **Report reproducibly.** Provide the protocol, model identifiers and dates, prompt and scoring versions, sample sizes, aggregation, uncertainty method, and enough artifacts for an independent check, subject to privacy, license, and provider restrictions.

## Output

Provide an audit table with finding, evidence, impact on interpretation, and recommended correction. Then give a short summary of claims that are supported, need qualification, or cannot yet be verified. Never fabricate recalculated values or claim checks that were not run.
