# Humanizer agent skill

A GitHub Copilot agent skill for rewriting and creating clear, accurate technical writing, documentation, explanations, and notes.

The skill is designed for source-grounded developer documentation, including structured cloud documentation with concepts, procedures, reference tables, code samples, limitations, and related links.

## Skill location

The project skill is located at:

```text
.github/skills/humanizer/
```

The directory contains `SKILL.md` and the supporting templates, style rules, and Google developer documentation style-guide index used by the skill.

## Install

Copy the `humanizer` directory into a project's `.github/skills/` directory, or install it with GitHub CLI from this repository after it is published:

```shell
gh skill install OWNER/REPOSITORY humanizer
```

Inspect a skill before installing it:

```shell
gh skill preview OWNER/REPOSITORY humanizer
```

## Validate and publish

With GitHub CLI 2.90.0 or later:

```shell
gh skill publish --dry-run
gh skill publish
```

Review the generated metadata and repository settings before publishing. This repository is released under the MIT License; see [LICENSE](LICENSE) for the full terms.

## Accuracy

The skill can produce documentation in the style and structure of Google Cloud or BigQuery guides when given reliable source material. It must not invent product behavior, commands, quotas, pricing, links, or version-specific details.
