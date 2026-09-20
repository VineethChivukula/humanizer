---
name: humanizer
description: "Rewrite or create clear, accurate technical writing, documentation, explanations, and notes. Use for structured product documentation, including cloud and developer guides, when source material must be preserved and the output should be natural, accessible, and easy to scan."
license: MIT
---

# Humanizer

Use this skill to make writing sound clear, natural, and appropriate for its audience without losing technical accuracy.

## What this skill does

- Rewrites dense or robotic writing into readable, conversational prose
- Converts rough notes into polished documentation
- Explains technical ideas for a broad audience without oversimplifying
- Keeps the tone appropriate, direct, and accessible
- Preserves correctness, structure, and clarity

## Core writing rules

- Prefer active voice and clear subject-verb structure.
- Write for the reader: explain why, not just what.
- Use short sentences and plain words when possible.
- Keep necessary jargon, but define it quickly.
- Use second person when it helps the reader follow along.
- Be concrete. Show examples and avoid vague claims.
- Avoid hype, filler, and exaggerated certainty.
- Make the structure easy to skim with headings, bullets, steps, and summaries.
- Use inclusive, respectful language and avoid assumptions.
- Keep terminology and formatting consistent.
- For product and developer documentation, prefer neutral, precise, instructional prose over warmth or conversational phrasing.

## Reference sources

- Google style guide index: ./index/google_style_guide_urls.csv
- Distilled rules: ./references/style-rules.md

For documentation work, use the index as a lookup map rather than treating it as background reading. Select the entries that match the requested output and apply their guidance before drafting or revising. At minimum, consult the relevant guidance for headings, procedures, links, and code when producing developer documentation. Also consult tables, notices, images, product names, dates and times, or accessibility when those features appear in the source or planned output.

Use the index categories as follows:

- **General Principles** for audience, tone, accessibility, inclusion, translation, and factual claims.
- **Language & Grammar** for terminology, voice, sentence structure, abbreviations, and word choice.
- **Formatting & Organization** for headings, lists, procedures, tables, code, commands, UI text, links, dates, and notices.
- **Images & Media** for figures, diagrams, screenshots, and alt text.
- **Reference & Special Topics** for API comments, product names, semantic markup, and specialized reference content.

When a linked style-guide page is unavailable, use the distilled rules as the fallback and avoid claiming that a rule was verified against the source.

## Documentation workflow

For substantial documentation, follow this sequence:

1. Identify the audience, goal, documentation type, target format, and available sources.
2. Select the relevant style-guide entries from the index.
3. Plan the heading hierarchy and decide which examples, tables, notices, diagrams, and related links the reader needs.
4. Draft from the supplied source material, keeping facts, recommendations, and examples distinct.
5. Review the result for factual support, terminology, links, code formatting, accessibility, and consistency.

## Output modes

### Documentation mode

Use for project documentation, personal documentation, or structured guides.

- First identify the documentation type: concept guide, how-to guide, reference, troubleshooting guide, or overview.
- Match the structure to the type instead of forcing every document into the same outline.
- Use a clear title and a short overview that establishes scope and audience.
- Explain why the topic matters when the reader needs context or a decision.
- Organize the body with headings that reflect the reader's questions and workflow.
- Include prerequisites, examples, verification, limitations, or related resources when they apply.
- End with a concise takeaway or a useful next step, such as related documentation.

#### Concept guide

- Define the subject and establish its scope.
- Explain when to use it and when to choose an alternative.
- Describe the core concepts, tradeoffs, and important operational considerations.
- Use examples, comparisons, tables, or diagrams when they make the relationships clearer.

#### How-to guide

- State the goal and expected result.
- List prerequisites, permissions, inputs, and assumptions.
- Give ordered steps with commands or code in fenced blocks.
- Explain how to verify the result and mention relevant troubleshooting or cleanup.

#### Reference

- Present syntax, parameters, allowed values, defaults, return values, errors, or limits as applicable.
- Use tables for structured comparisons and keep examples close to the item they illustrate.
- Distinguish required values, optional values, and recommended values.

#### Troubleshooting guide

- Start with the symptom or error message.
- Explain likely causes and how to distinguish them.
- Give focused resolution steps and a way to confirm the fix.

### Explanation mode

Use for concepts, technical topics, or difficult ideas.

- Plain-language definition
- Why it matters
- How it works
- Example or analogy
- Key takeaways

### Notes mode

Use for turning rough thoughts into concise, useful notes.

- Topic
- Key ideas
- Important details
- Questions or uncertainties
- Next steps

## Technical documentation requirements

When the output is intended to resemble product documentation, apply these rules in addition to the writing rules above:

- Preserve meaningful links, link labels, code formatting, tables, diagrams, admonitions, and metadata when editing existing content.
- Use Markdown headings, lists, tables, fenced code blocks, and callouts consistently.
- Separate definitions, factual behavior, recommendations, examples, and warnings so readers can tell them apart.
- State prerequisites, supported inputs, defaults, limits, permissions, pricing, security, and compatibility details when they affect the task.
- Prefer precise product terminology over friendly paraphrases when the terminology is part of an API, command, UI label, or configuration.
- Add a "What's next" or related-resources section when the document is part of a larger documentation set.
- Match the target product's tone. For cloud and developer documentation, prefer direct, neutral, instructional prose over overly conversational language.

## Source and accuracy behavior

- Treat supplied documentation, code, schemas, and links as the source of truth for product-specific claims.
- Do not invent commands, API fields, limits, pricing, version behavior, citations, or links.
- If the source is missing or uncertain, state the assumption or mark the detail for verification instead of presenting it as fact.
- Preserve version-specific and date-specific qualifications.
- When creating new technical documentation from a source, distinguish source-backed facts from proposed examples or recommendations.

## Output contract

Before writing, infer or ask for the audience, documentation type, target format, and source material when they are not clear. For a large technical page, produce a structure that can support:

- A title and overview
- A contents-oriented heading hierarchy
- Conceptual explanation and decision guidance
- Examples, commands, or configuration snippets
- Tables or diagrams where useful
- Limitations, quotas, security, pricing, or troubleshooting where relevant
- Related links and next steps

Do not add sections merely to satisfy this list. Include each section only when it serves the reader or is supported by the source.

## Editing behavior

- Keep the original meaning unless the user asks for a change.
- Remove redundancy and filler.
- Smooth awkward transitions.
- Replace abstract wording with direct wording.
- Improve readability without sounding artificial or overly casual.
- Preserve technical precision and non-negotiable facts.

## Templates

- ./assets/documentation-template.md
- ./assets/explanation-template.md
- ./assets/notes-template.md

## Quality bar

The result should sound like a knowledgeable human wrote it: clear, honest, easy to read, respectful, accessible, and confident without sounding inflated. For product documentation, it should also be scannable, source-grounded, structurally complete, and neutral in tone.
