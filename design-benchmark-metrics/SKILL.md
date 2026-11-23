---
name: design-benchmark-metrics
description: Use when choosing or designing evaluation metrics for an LLM benchmark, especially when generic accuracy or F1 doesn't capture what failure costs in the domain. Trigger whenever the user is deciding how to score model outputs, asking about human evaluation protocols, or questioning whether a metric fits the task. Consider if there is a need to introduce new metrics or modify the scoring system.
---

# Design Domain-Appropriate Metrics

## Purpose
Pick metrics that reflect what failure actually means in this domain rather than defaulting to generic accuracy or F1, which reviewers will flag as insufficient for most domain-specific tasks.

## Process
1. Define the unit being scored and the consequences of different error types. Select metrics that reflect the task and intended use; explain any weighting or threshold choices.
2. For generated outputs, validate automatic metrics against the target behavior. Add human evaluation when it answers an important question, using a documented rubric, sampling plan, and rater qualifications appropriate to the task.
3. If confidence estimates affect the use case, assess calibration with a method suited to the data and decision. Confidence reporting is not relevant to every benchmark.
4. Plan uncertainty reporting based on the data and run design. Distinguish variation across items, prompts, model runs, and annotators; choose intervals or summaries that match the sampling assumptions.

## Output
A metrics specification with primary and secondary metrics, interpretation, scoring rules, human rubric if applicable, calibration plan if relevant, and uncertainty method.

## Pitfalls
- Metrics can hide tradeoffs. Pair an aggregate with relevant error rates or slices when those distinctions matter and the sample supports them.
- Metric choice does not make the benchmark valid by itself. State what the score captures and what remains outside the measure.
