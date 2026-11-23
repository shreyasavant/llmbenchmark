---
name: analyze-benchmark-errors
description: Use after baseline experiments are run, to perform the error and failure analysis that distinguishes a strong benchmark paper from a leaderboard table. Trigger whenever the user has results and needs to explain what they reveal, or is preparing the analysis/discussion section.
---

# Analyze Errors and Failure Modes

## Purpose
Explain what the observed failures reveal about model behavior and the benchmark's measurement limits. Separate measured patterns from hypotheses about why they occur.

## Process
1. Group errors using the task taxonomy or a transparent scheme grounded in the examples. Report counts and denominators; note categories that overlap or cases that cannot be categorized reliably.
2. Identify plausible shortcuts the benchmark may reward, such as lexical overlap or answer-position bias. Prioritize probes that fit the format and could change interpretation; distinguish checks performed from risks not tested.
3. Inspect a documented sample of failures. Choose the sample based on task size and analysis goals, and describe how it was selected. Avoid treating a few illustrative cases as prevalence estimates.
4. Run ablations or slice analyses where the data and budget support them. Interpret subgroup results cautiously when samples are small or not representative.

## Output
An error taxonomy with counts and denominators where possible, any shortcut or ablation checks performed, and a qualitative discussion of representative examples and limitations.

## Pitfalls
- Error categories are partly shaped by the taxonomy and reviewer. Explain ambiguous cases and avoid overstating causal explanations.
- A shortcut check can rule out only the tested shortcut under the tested conditions. Report its scope rather than claiming the benchmark is free of bias.
