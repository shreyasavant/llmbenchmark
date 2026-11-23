---
name: run-benchmark-experiments
description: Use when actually executing the benchmark evaluation runs across models and conditions. Trigger whenever the user is setting up evaluation infrastructure, running models against the benchmark, or asking how to make benchmark results reproducible. Focus on reproducibility, detailed logging, and controlled experiment design to ensure that results are reliable and can be independently verified.
---

# Run Experiments with Reproducibility Built In

## Purpose
Generate results that another team could reproduce from the paper alone, and that hold up if scrutinized after publication.

## Process
1. Define the comparison conditions and rationale. Match prompts and decoding settings when the goal is a controlled comparison; if settings differ by design, state why and avoid implying a matched comparison.
2. Record model/provider identifiers, access dates, prompts, tools, context, decoding, retry behavior, software and evaluation versions, and relevant budget limits. Note when providers do not expose an exact model snapshot.
3. Retain raw outputs and per-example records when permitted and proportionate to privacy, licensing, and storage constraints. Otherwise retain a documented, auditable representation and explain what cannot be reproduced.
4. Decide whether repeated runs, seeds, prompt variants, or bootstrap estimates are appropriate for the source of uncertainty. Use enough repetitions for the intended inference when feasible, and report the design and spread or interval.
5. Log failures, refusals, timeouts, malformed outputs, and exclusions. Predefine how they are handled and include their counts.

## Output
A results table with uncertainty reporting appropriate to the design, available per-example records, and a versioned record of model and prompt configurations, failures, and exclusions.

## Pitfalls
- Hosted models and APIs can change. Record the provider's model identifier and evaluation date, and avoid promising exact rerun equivalence when snapshots are not available.
- Raw outputs may contain sensitive or licensed material. Apply the project's retention and access rules; if full outputs cannot be retained, document that limitation and the evidence kept for auditing.
