---
name: survey-existing-benchmarks
description: Use to build the related-work comparison and confirm the benchmark gap actually holds. Trigger whenever the user needs related work for a benchmark paper, wants to check whether a benchmark already exists, or needs a benchmark comparison table for a draft.
---

# Survey Existing Benchmarks

## Purpose
Produce a comparison table that does three jobs at once: confirms the gap identified earlier still holds, becomes the related-work section, and clarifies which benchmarks are the closest prior work to cite.

## Process
1. Search systematically using the domain with "benchmark", "dataset", and "evaluation", and follow citations from relevant general benchmarks. If browsing is available, favor original papers, dataset cards, and official benchmark documentation; record source links and search date.
2. For each relevant benchmark, record available information such as name, domain, task type, size, data and evaluation versions, metrics, and stated limitations. Investigate contamination evidence when relevant; distinguish reported checks, independent findings, and unknown status.
3. Sort the table by relevance, not chronology — closest prior work goes first in both the table and the prose.
4. Re-check the gap paragraph against this completed table. If something here already closes the gap, narrow the claim or explicitly differentiate against it.

## Output
A Markdown or LaTeX table with benchmark, domain, task type, size/version, metrics, contamination evidence or unknown status, and key limitation, with citations to the sources used.

## Pitfalls
- Don't only search for benchmarks framed as "LLM benchmarks" — older, pre-LLM datasets in the same domain are often the actual closest comparison and get missed.
- A lack of published contamination evidence does not show that a benchmark is contaminated or clean. Label the status as unknown when evidence is unavailable.
