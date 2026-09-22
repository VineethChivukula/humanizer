# Humanizer agent skill

Humanizer is a GitHub Copilot agent skill for rewriting and creating clear,
accurate technical writing. It helps produce documentation, explanations, and
notes that are readable, structured, and appropriate for their audience.

The skill is designed for source-grounded developer documentation. It can help
turn reliable source material into concept guides, how-to guides, reference
pages, troubleshooting guides, project documentation, and concise notes.

## When to use Humanizer

Use Humanizer when you need to:

- Rewrite dense, robotic, or inconsistent prose.
- Turn rough notes into useful documentation.
- Explain a technical subject without removing important detail.
- Structure a developer guide with procedures, code samples, tables, links, or
  troubleshooting information.
- Review technical writing for clarity, accessibility, consistency, and
  unsupported claims.

The skill preserves the supplied meaning and technical constraints. It does not
replace missing source material or verify product behavior that the source does
not establish.

## How it works

For a documentation request, Humanizer:

1. Identifies the audience, goal, document type, target format, and available
   sources.
2. Selects relevant guidance from the bundled style-guide index.
3. Plans a heading hierarchy and the examples, tables, notices, or links the
   reader needs.
4. Drafts in the order the reader needs the information.
5. Reviews the result for factual support, terminology, formatting,
   accessibility, and consistency.

The skill separates concepts, procedures, reference information, warnings, and
recommendations so readers can distinguish what a feature does from what they
should do.

## Output modes

Choose the mode that matches the reader's task:

| Mode          | Use it for                                  | Typical structure                                                      |
| ------------- | ------------------------------------------- | ---------------------------------------------------------------------- |
| Documentation | Project documentation and structured guides | Overview, prerequisites, task or concept, verification, and next steps |
| Explanation   | Technical concepts and difficult ideas      | Definition, importance, mechanism, example, and takeaways              |
| Notes         | Rough thoughts that need structure          | Topic, key ideas, details, questions, and next steps                   |

Documentation mode also supports these page types:

- **Concept guide:** Defines a subject, explains when to use it, and covers
  tradeoffs and operational considerations.
- **How-to guide:** States a goal, lists prerequisites, gives ordered actions,
  and explains how to verify the result.
- **Reference:** Documents syntax, parameters, allowed values, defaults, limits,
  errors, or comparisons.
- **Troubleshooting guide:** Starts with a symptom, distinguishes likely causes,
  and provides focused resolution and verification steps.

## Example requests

Give the skill the source material and the intended outcome. For example:

```text
Rewrite this API guide for developers who are new to the service. Keep the
commands and behavior accurate, add prerequisites and verification, and flag
any details that are not supported by the source.
```

```text
Turn these meeting notes into a concise technical design note. Separate facts,
decisions, open questions, and next steps. Do not resolve missing information.
```

For product-specific documentation, include the relevant source documents, code,
schemas, links, or version details in the request. The skill treats those inputs
as the source of truth.

## Writing principles

Humanizer follows these principles:

- Prefer active voice, short sentences, and plain language.
- Define necessary jargon before relying on it.
- Use descriptive, sentence-case headings and a logical hierarchy.
- Use imperative verbs for procedures and one meaningful action per step.
- Introduce code samples and explain placeholders and expected results.
- Use selective, descriptive links instead of raw URLs or vague link text.
- Qualify claims about performance, cost, security, reliability, and compatibility.
- Use notes and warnings only when the information falls outside the main flow
  or describes a material risk.
- Keep uncertainty visible instead of filling gaps with invented details.

## Repository contents

The distributable skill is located in [`skills/humanizer/`](skills/humanizer/).

| Path                                                                                      | Purpose                                                                   |
| ----------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| [`SKILL.md`](skills/humanizer/SKILL.md)                                                   | Skill metadata, workflow, writing rules, output modes, and quality checks |
| [`assets/documentation-template.md`](skills/humanizer/assets/documentation-template.md)   | Template for structured documentation                                     |
| [`assets/explanation-template.md`](skills/humanizer/assets/explanation-template.md)       | Template for technical explanations                                       |
| [`assets/notes-template.md`](skills/humanizer/assets/notes-template.md)                   | Template for structured notes                                             |
| [`references/style-rules.md`](skills/humanizer/references/style-rules.md)                 | Distilled writing and documentation rules                                 |
| [`index/google_style_guide_urls.csv`](skills/humanizer/index/google_style_guide_urls.csv) | Lookup index for relevant Google developer documentation guidance         |

The index is a lookup map, not a requirement to read every linked page. The
skill selects guidance based on the requested output, such as headings,
procedures, links, code, tables, notices, images, or accessibility.

## Install

Copy the `humanizer` directory into a project's `.github/skills/` directory, or
install it with GitHub CLI from this repository after it is published:

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

Review the generated metadata and repository settings before publishing. The
skill metadata declares the MIT license; see [LICENSE](LICENSE) for the full
terms.

## Accuracy and limitations

Humanizer can produce documentation in the style and structure of maintained
cloud or developer documentation when given reliable source material. It must
not invent product behavior, commands, API fields, quotas, pricing, links, or
version-specific details.

When information is missing, conflicting, or version-sensitive, the resulting
document should state the assumption or identify the detail for verification.
