---
name: curate-benchmark-data
description: Use when collecting, annotating, and quality-controlling the raw data for an LLM benchmark. This is the highest-stakes step for the paper's credibility. Trigger whenever the user is sourcing data, writing an annotation guide, deciding between real and synthetic data, or asking about licensing for benchmark data.
---

# Curate Benchmark Data

## Purpose
Build the dataset in a way that survives reviewer scrutiny on provenance, quality, and licensing. This is what gets trusted (or not) more than almost anything else in the paper.

## Process
1. Select and document data sources based on task fit, representativeness, feasibility, and permitted use. Synthetic or model-generated data can be useful, but label it and validate the properties relevant to the benchmark's claims.
2. Before annotation, draft task instructions, decision rules for likely edge cases, and worked examples. Pilot the guide and revise ambiguous criteria.
3. For multiple annotators, calibrate on shared examples. Choose agreement or adjudication methods appropriate to the labels and sampling; report their assumptions and limitations. Agreement alone does not establish correctness.
4. Document filtering, deduplication, privacy and safety review, and quality checks. Set manual review rates based on data risk and available resources, and disclose the sampling method and findings.
5. Track provenance and applicable terms or licenses for each source. Confirm that collection, processing, and intended release are permitted; consult a qualified reviewer when rights are unclear.

## Output
Annotation guide, calibration and quality-control evidence, filtering records, and a source-provenance and permissions manifest.

## Pitfalls
- Agreement scores depend on label prevalence, sampling, and the statistic used. Interpret them with the task and adjudication process rather than as a universal quality threshold.
- Permission to access data does not automatically grant permission to redistribute it or publish model inputs and outputs. Review each use and release separately.
