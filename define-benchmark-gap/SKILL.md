---
name: define-benchmark-gap
description: Use this skill at the very start of any LLM benchmark paper project, before any data collection begins. It identifies and stress-tests the gap the benchmark fills relative to existing work. Trigger whenever the user wants to start a new benchmark, has an idea for a benchmark, or asks whether a benchmark is worth building.
---

# Define the Benchmark Gap

## Purpose
Establish, in one defensible paragraph, what existing benchmarks cannot measure that this one will. This is the thesis the entire paper has to support, so get it right before touching data.

## Process
1. Search for relevant benchmarks, datasets, and evaluation protocols in the target and adjacent domains. When browsing is available, prefer primary sources and record links and dates.
2. For each, note: task type, what it measures, known limitations (contamination, narrow scope, static/saturating, missing a domain constraint).
3. Classify the gap into one of these defensible categories. If it doesn't fit cleanly, the case is weak — go back to step 1.
   - Reasoning gap: existing benchmarks test recall/knowledge, not domain-specific multi-step reasoning
   - Contamination gap: existing benchmarks are static and likely memorized
   - Constraint gap: existing benchmarks ignore a real-world constraint of the domain (long context, tool use, multi-turn, partial observability, real-time/streaming data)
   - Coverage gap: no benchmark exists for this domain/task pair at all
4. Draft the gap paragraph: one sentence on what's missing, one sentence on why it matters in this domain, one sentence on what this benchmark will measure instead.
5. Pressure-test it against the comparison: if prior work already addresses the proposed gap, narrow the claim or explain the meaningful distinction. Keep unresolved areas explicit rather than assuming absence.

## Output
A single paragraph (3-5 sentences) plus the comparison list from step 2, ready to seed both the introduction and the related-work table.

## Pitfalls
- "No benchmark exists" is rarely literally true — say what's adjacent and why it doesn't transfer.
- Don't conflate "this hasn't been done" with "this matters." Justify why the gap matters operationally in the domain, not just academically.
