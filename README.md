# Solution Research

An agent skill for researching and choosing an approach before implementation.

[中文说明](README.zh-CN.md) · [Skill instructions](SKILL.md) · [Related skills](docs/related-skills.md)

Use it when a substantial new feature, tool, or workflow still has an open implementation choice. It checks the existing environment, researches viable approaches, compares the trade-offs, and recommends a direction with supporting sources.

## What it delivers

- A recommendation grounded in the user's goals and constraints.
- Usually 2–4 viable alternatives, with a concise comparison.
- Direct sources for decision-critical claims and visible evidence gaps.
- A focused choice when the user still needs to decide, or continuation when the user has already chosen or delegated the choice.

Routine fixes, small edits, and fully specified execution do not automatically trigger a new selection process. A research-only request ends with the research result.

## Install

Download or clone this repository. Place its contents in a directory named `solution-research` inside your agent's configured skill directory. The directory must contain `SKILL.md` at its root; it may also include `agents/openai.yaml` for hosts that use that metadata.

If a skill with the same name is already installed, compare the instructions before replacing it. Follow your agent's own discovery or reload procedure.

## Use

```text
Use $solution-research to compare approaches for adding offline search
to our desktop application. Keep our existing stack and minimize
ongoing maintenance. Recommend an approach with sources and trade-offs.
```

The instruction file is written in Chinese and asks the agent to respond in the user's language. Search, page-reading, repository, and question tools are selected from the host's available capabilities. When external sources cannot be checked, the result must identify which conclusions are provisional.

## Contents

```text
solution-research/
├── SKILL.md
├── agents/openai.yaml
├── README.md
├── README.zh-CN.md
└── docs/related-skills.md
```

This is an instruction skill, with no executable runtime or required package dependencies. Validation covers its structure and a static review of decision boundaries; cross-agent behavioral testing has not been performed.

## Versions

- [v1.0.0](https://github.com/okayyoo/solution-research/tree/v1.0.0): the original skill, preserved as the first commit.
- [v1.1.0](https://github.com/okayyoo/solution-research/tree/v1.1.0): refined decision boundaries, evidence requirements, tool portability, and documentation.

[Commit history](https://github.com/okayyoo/solution-research/commits/main/) · [Compare versions](https://github.com/okayyoo/solution-research/compare/v1.0.0...v1.1.0)
