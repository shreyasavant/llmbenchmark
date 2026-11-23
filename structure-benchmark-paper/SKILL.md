---
name: structure-benchmark-paper
description: Use when drafting or organizing the full manuscript for an LLM benchmark paper. Trigger whenever the user is writing the paper itself, deciding section order, or asking how a benchmark paper should be structured for submission.
---

# Structure the Paper

## Purpose
Organize the manuscript in the order reviewers expect for a benchmark/dataset paper, so the construction and evaluation work already done lands clearly.

## Process
Use this section order, adapting depth to venue page limits:
1. Introduction — state the gap, list contributions explicitly, lead with the headline result.
2. Related work — the benchmark comparison table, ordered by relevance not chronology.
3. Task definition and benchmark construction — the locked schema, taxonomy, and data curation methodology.
4. Dataset statistics and quality control evidence — sizes, splits, agreement scores, filtering pipeline summary.
5. Evaluation protocol and metrics — chosen metrics with justification, human eval rubric if used.
6. Experiments — the baseline results table.
7. Analysis — error analysis, bias/shortcut checks, contamination check results, any ablations.
8. Limitations — specific, not generic; state exactly what wasn't tested and why.
9. Ethics/broader impact — required if the domain is sensitive (health, hiring, finance, safety-critical infrastructure).

## Output
A full draft following this structure, with each section pulling directly from the artifacts produced earlier (gap paragraph, comparison table, task spec, curation docs, metrics spec, results table, error taxonomy).

## Pitfalls
- Writing limitations as boilerplate ("future work could explore more languages") reads as an afterthought — tie each limitation to a specific, checked decision made earlier in the project.
- Don't bury the benchmark construction methodology in an appendix if it's central to the contribution; reviewers expect it in the main body for a dataset/benchmark paper.
