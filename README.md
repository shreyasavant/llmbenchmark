# LLM Benchmarking Skills

A practical collection of agent skills for designing, running, and reporting rigorous evaluations of large language models. The skills guide the full lifecycle: from deciding what to measure through data curation, experiment design, analysis, and release.

The collection is intended for Claude Code, Codex, and other agents that support the open Agent Skills `SKILL.md` format. Skills are plain Markdown instructions. This repository does not include install scripts, executable hooks, or required dependencies.

## Skills

| Skill | Use it to |
|---|---|
| [llm-benchmarking](llm-benchmarking/SKILL.md) | Plan and navigate an end-to-end LLM benchmark project. |
| [define-benchmark-gap](define-benchmark-gap/SKILL.md) | Establish what existing benchmarks fail to measure. |
| [survey-existing-benchmarks](survey-existing-benchmarks/SKILL.md) | Build a sourced comparison of relevant benchmarks. |
| [scope-benchmark-task](scope-benchmark-task/SKILL.md) | Specify tasks, schemas, difficulty, and exclusions. |
| [curate-benchmark-data](curate-benchmark-data/SKILL.md) | Source, annotate, quality-check, and license data. |
| [build-benchmark-splits](build-benchmark-splits/SKILL.md) | Create defensible splits and assess contamination risks. |
| [design-benchmark-metrics](design-benchmark-metrics/SKILL.md) | Choose task-appropriate metrics and uncertainty reporting. |
| [select-benchmark-baselines](select-benchmark-baselines/SKILL.md) | Choose comparison systems and evaluation conditions. |
| [run-benchmark-experiments](run-benchmark-experiments/SKILL.md) | Plan reproducible model evaluations and retain usable records. |
| [audit-benchmark-results](audit-benchmark-results/SKILL.md) | Check results, comparisons, uncertainty, and claims before sharing. |
| [analyze-benchmark-errors](analyze-benchmark-errors/SKILL.md) | Find recurring failures and benchmark shortcuts. |
| [structure-benchmark-paper](structure-benchmark-paper/SKILL.md) | Organize a benchmark manuscript around its evidence. |
| [select-benchmark-venue](select-benchmark-venue/SKILL.md) | Match the contribution to a venue and its requirements. |
| [plan-benchmark-release](plan-benchmark-release/SKILL.md) | Prepare a reproducible, maintainable release. |

## Install

Copy the skill folders you need into your agent's project-level skills directory. For Claude Code, use `.claude/skills/`; for Codex, use `.agents/skills/`. For example:

```sh
cp -R define-benchmark-gap .claude/skills/
cp -R run-benchmark-experiments .claude/skills/
```

You can also clone this repository and point your agent at the relevant `SKILL.md` files. Review the Markdown before adopting a skill, especially in projects where agent instructions can access sensitive files or run commands. These skills are guidance, not a security boundary; review any proposed commands and data handling yourself.

## Suggested workflow

Start with `define-benchmark-gap`, then survey prior work and lock the task scope before collecting data. Curate data and define splits, metrics, and baselines before running experiments. Audit and analyze the results before drafting a paper or preparing a public release. The [llm-benchmarking skill](llm-benchmarking/SKILL.md) helps adapt that sequence to the project.

Not every project needs every step. Tailor the workflow to the task, risk, resources, and intended claims; document justified deviations instead of treating checklists as universal requirements.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Suggestions and focused improvements are welcome, particularly corrections to evaluation guidance, examples, and install compatibility.

## License

MIT. See [LICENSE](LICENSE).
