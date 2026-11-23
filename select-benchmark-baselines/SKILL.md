---
name: select-benchmark-baselines
description: Use when choosing which models and conditions to evaluate as baselines for an LLM benchmark. Trigger whenever the user is deciding which models to test, whether to include human performance, or how to set up zero-shot vs few-shot vs fine-tuned comparisons.
---

# Select Baselines Deliberately

## Purpose
Build a baseline set that gives the results table interpretive power, not just a leaderboard of scores.

## Process
1. Choose baselines that answer the research or product question. Depending on the task, consider simple heuristics, random or majority baselines, prior systems, open-weight and hosted models, or human performance.
2. Select a relevant range of model capabilities and access types within the available budget. Explain omissions, model selection criteria, and model versions or evaluation dates.
3. Choose zero-shot, few-shot, fine-tuned, tool-assisted, or other conditions only when they clarify the question. Match conditions for controlled comparisons, or explicitly identify differences that limit interpretation.
4. Consider expert or user performance when it is feasible, ethical, and meaningful for the task. Define the human protocol and compare like with like; do not treat human results as a required anchor for every benchmark.

## Output
A baseline matrix of model x relevant condition x metric, including model identifiers, dates, access type, and protocol details. Add human results if collected and relevant.

## Pitfalls
- Differences in model access, prompts, tuning, or compute can affect scores. Report them and qualify comparisons instead of treating the ranking as an intrinsic model property.
- Human evaluation can add useful context, but its value depends on task, sampling, expertise, and protocol. State limitations and do not overgeneralize from a small or convenience sample.
