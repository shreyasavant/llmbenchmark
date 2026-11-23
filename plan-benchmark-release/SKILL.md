---
name: plan-benchmark-release
description: Use when planning how an LLM benchmark will be released and maintained after publication. Trigger whenever the user is preparing a dataset for public release, setting up a leaderboard, deciding on licensing, or planning benchmark versioning.
---

# Plan the Release Package

## Purpose
Maximize the benchmark's long-term impact, which depends more on the release package than on the writing quality of the paper itself.

## Process
1. Choose a release license only after checking rights and terms for source data, annotations, prompts, outputs, and code. When terms or privacy obligations are unclear, seek qualified advice before release.
2. Package a versioned evaluation implementation with documented preprocessing, scoring, dependencies, and known limitations. Preserve a reference version so future changes do not silently alter earlier results.
3. Decide whether a leaderboard or results table fits the project and who can maintain it. Define submission, verification, and update policies before accepting external results.
4. Document benchmark versioning and how scores across versions should be compared. Plan a refresh only if the task's stability, contamination risk, and maintenance capacity justify it.
5. Review privacy, security, misuse, and data leakage risks before releasing prompts, examples, outputs, or evaluation code.

## Output
A release plan stating what can be shared, under which terms, with versioned evaluation materials, an optional leaderboard policy, and a maintenance and versioning plan.

## Pitfalls
- Check that the license covers the actual materials being released; a repository license alone does not relicense third-party data.
- A public test set may enable memorization or tuning. Consider whether hidden evaluation, rotating sets, or other controls are appropriate and feasible for this project.
