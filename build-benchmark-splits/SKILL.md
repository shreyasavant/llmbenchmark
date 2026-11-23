---
name: build-benchmark-splits
description: Use when partitioning benchmark data into train/validation/test and checking for pretraining contamination. Trigger whenever the user is creating data splits for an LLM benchmark, worried about test set leakage, or deciding whether the benchmark should be static or dynamic/rolling.
---

# Build Benchmark Splits with Contamination Controls

## Purpose
Make sure the held-out test set is actually held out, and that the benchmark has a credible answer to "how do you know models haven't already seen this."

## Process
1. Define split units and grouping before splitting. Keep related examples (for example, same source document, user, or conversation) together when cross-split leakage would inflate scores.
2. Where feasible, reserve the test set before model or prompt development and keep a separate development set. If test access cannot be restricted, document how repeated inspection may have influenced decisions.
3. Assess plausible contamination sources based on data age, public availability, task format, and model training cutoffs. Use suitable overlap checks or memorization probes when feasible; state what each check can and cannot detect.
4. Choose static or versioned evaluation data based on task stability, contamination risk, and comparability needs. Record versioning rules before comparing results across releases.
5. Report split construction, sizes, grouping, checks performed, findings, and known limitations. A failed or inconclusive check should be described accurately.

## Output
Split definitions or files with sizes, grouping rules, a contamination assessment with limitations, and an update/versioning policy where relevant.

## Pitfalls
- No single contamination check establishes that examples were absent from pretraining. Describe the evidence and residual uncertainty rather than claiming a clean test set.
- Repeatedly using test results to tune prompts or examples weakens the held-out claim. Prefer a separate development set and document any test feedback that influenced the protocol.
