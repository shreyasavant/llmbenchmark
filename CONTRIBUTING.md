# Contributing

Contributions that improve the accuracy, clarity, or usability of these LLM benchmarking skills are welcome.

## Skill format

- Keep one focused skill per directory with a `SKILL.md` file.
- Include valid YAML frontmatter with a short, specific `name` and a `description` that tells an agent when to use the skill.
- Write actionable steps and concrete expected outputs.
- Distinguish recommendations from requirements. Avoid universal sample-size thresholds or procedures unless they are justified for the task.
- Tell the agent to separate evidence from assumptions, cite sources for time-sensitive claims, and avoid claiming checks it did not perform.
- Keep skills as readable Markdown. Do not add install-time scripts, credential collection, telemetry, or hidden network behavior.

## Changes

Keep pull requests focused. Explain which benchmark workflow or agent compatibility the change improves. If adding examples, use synthetic or openly licensed material and identify it as such. Do not include private datasets, credentials, or unpublished evaluation data.
