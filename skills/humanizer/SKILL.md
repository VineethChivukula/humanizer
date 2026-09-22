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

## Developer documentation style

For documentation, notes, and explanations, write like a maintained developer
documentation set. Use these patterns as the default quality bar. They are informed
by the Google developer documentation style guide and high-quality product
documentation, but do not copy source wording or force the same structure onto
unrelated content.

- Open with a short definition or purpose statement. Tell the reader what the
  subject is and what it helps them understand or do before explaining details.
- Make the first useful decision easy to find. Include a "When to use" or
  "Choose ... when" section when the reader must select among approaches,
  configurations, or alternatives.
- Explain the mechanism before presenting edge cases. Define important objects,
  relationships, boundaries, and terms in the order the reader needs them.
- Separate concept, procedure, reference, and troubleshooting content. Do not mix
  facts, instructions, recommendations, and warnings into one paragraph.
- Use operational headings when the subject supports them: limitations, constraints,
  compatibility, risks, troubleshooting, and what's next.
- State tradeoffs and alternatives directly. Explain when a related feature is a
  better fit, what it changes, and what the reader gives up.
- Prefer qualified, verifiable claims. Use "can", "helps", "typically", or
  "might" when behavior depends on context. Do not promise performance, savings,
  security, correctness, or compatibility without source support.
- Keep examples concrete and small. Introduce each example, show the relevant
  input, code, or scenario, explain the important result, and omit unrelated
  scaffolding.
- Use present tense for behavior and imperative verbs for actions. Avoid
  conversational asides, rhetorical questions, marketing language, and filler.

### Default concept workflow

Use this workflow for a request such as "Explain transient tables" unless the user
asks for a different format:

1. Identify the subject, audience, purpose, and source of truth. If the request is
   ambiguous, make a reasonable assumption and state it briefly.
2. Choose the document type: concept guide, how-to guide, reference, troubleshooting
   guide, project documentation, or notes.
3. Open with a direct definition and scope statement. Do not begin with "In this
	article" or a broad history lesson.
4. Explain when the subject applies, when it does not, and what alternatives exist
   when those distinctions help the reader decide.
5. Explain how it works from the reader's point of view. Introduce terms before
   relying on them and explain cause and effect.
6. Add a concrete example, comparison, code sample, or scenario. Explain what the
	example demonstrates and do not present illustrative values as universal rules.
7. State important constraints, limitations, risks, assumptions, and unresolved
	questions. Separate facts from recommendations.
8. End with a concise takeaway and the next useful action or related topic.
9. Review the result against the style guide and remove unsupported claims,
	repetition, vague transitions, and sections that do not serve the reader.

### Page architecture

Choose the smallest structure that serves the reader. For a substantial technical
page or explanation, use this sequence when applicable:

1. Definition and scope
2. When to use it or how to choose it
3. Core behavior or how it works
4. Types, options, or decision criteria
5. Example or procedure
6. Limitations, constraints, risks, and compatibility
7. Troubleshooting or verification
8. What's next

Do not add a section just to complete the sequence. A concept page might omit a
procedure; a reference page might begin with syntax; a short how-to might need only
prerequisites, steps, verification, and related links.

### Headings, links, and notices

- Use sentence case and a logical heading hierarchy. Use noun phrases for concepts
	and base-form verbs for tasks, such as "Partition pruning" and "Create a table".
- Make headings descriptive and unique. Do not put links in headings or use
	headings merely to change visual appearance.
- Link selectively to the most relevant destination. Use descriptive link text and
  avoid "click here", "this document", raw URLs, and duplicate links.
- Keep necessary context on the current page. Link out for deeper, nonessential
	detail or another product's authoritative documentation.
- Use a note only for useful information outside the main flow that readers can
	skip and still succeed. Use a caution for a material risk and a warning for
	possible data loss, security exposure, or another serious consequence.
- Do not hide prerequisites, required actions, expected results, or ordinary
	cross-references in a note.

### Procedures and code

- State the goal and prerequisites before the steps. Identify the tool or
  environment in the step before the action: "In Cloud Shell, create ... ."
- Use one step per meaningful action, keep steps short, and use a single best path
	unless alternatives are necessary for the audience.
- Start each step with an imperative verb. Mark optional steps with "Optional:".
- Introduce commands and code samples with what they accomplish. Explain
	placeholders immediately after the sample and describe output only when it helps
	the reader continue.
- Use fenced code blocks with a language identifier when the target format supports
  them. Keep samples runnable or clearly label pseudocode and omitted sections.

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
5. Draft in the order the reader needs the information, not the order in which the source presents it.
6. Review the result for factual support, terminology, links, code formatting, accessibility, and consistency.
7. Perform a documentation pass: confirm the opening definition, decision guidance,
   prerequisites, examples, verification, limitations, and next steps.

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
- Identify the execution environment, explain placeholders, and keep each step focused on one action.
- Explain how to verify the result and mention relevant troubleshooting or cleanup.

#### Reference

- Present syntax, parameters, allowed values, defaults, return values, errors, or limits as applicable.
- Use tables for structured comparisons and keep examples close to the item they illustrate.
- Distinguish required values, optional values, and recommended values.

#### Troubleshooting guide

- Start with the symptom or error message.
- Explain likely causes and how to distinguish them.
- Give focused resolution steps and a way to confirm the fix.

#### Project documentation

- Describe what the project, module, service, or workflow does and who depends on it.
- Document the normal path first: prerequisites, setup, usage, expected results, and
	verification.
- Use the repository's own names, commands, APIs, and conventions. Inspect the code
	before making claims about behavior.
- Document configuration, boundaries, failure modes, maintenance tasks, and related
	components when they affect a reader's work.
- End with troubleshooting, extension points, or the next related task as appropriate.

### Explanation mode

Use for concepts, technical topics, or difficult ideas.

- Use the default concept workflow. The output should read like a concise concept
	guide, not an informal chat response.
- Prefer a precise example or comparison over an analogy. Use an analogy only when
	it clarifies the mechanism without introducing a misleading mental model.
- Distinguish what is true, what is recommended, what is illustrative, and what is
	uncertain.
- Use headings when the explanation has more than a few paragraphs. Keep the
	explanation proportional to the complexity of the subject.
- End with a short takeaway and a next question or related concept when useful.

### Notes mode

Use for turning rough thoughts into concise, useful notes.

- Treat notes as small documentation pages, not an unstructured dump.
- Start with the topic and a one-sentence purpose or definition.
- Group related facts under descriptive headings and preserve the distinction between
	facts, decisions, open questions, and proposed actions.
- Use bullets for parallel points, numbered lists for sequence, and tables only for
	genuine comparisons.
- Keep uncertainty visible. Do not resolve missing information by inventing facts.
- End with explicit decisions, questions, owners, or next steps when the source
	provides them.

## Technical documentation requirements

Apply these rules to documentation, notes, and explanations when the output contains
technical or project-specific information:

- Preserve meaningful links, link labels, code formatting, tables, diagrams, admonitions, and metadata when editing existing content.
- Use Markdown headings, lists, tables, fenced code blocks, and callouts consistently.
- Separate definitions, factual behavior, recommendations, examples, and warnings so readers can tell them apart.
- State prerequisites, supported inputs, defaults, limits, permissions, risks, and compatibility details when they affect the task.
- Prefer precise product terminology over friendly paraphrases when the terminology is part of an API, command, UI label, or configuration.
- Add a "What's next" or related-resources section when the document is part of a larger documentation set.
- Match the target product's tone. For technical documentation, prefer direct,
  neutral, instructional prose over overly conversational language.
- Use a predictable information order: what it is, when it applies, how it works,
  how to use it, and what constraints apply.
- Explain relationships between adjacent features instead of treating each feature
	as isolated. Include a comparison or selection rule when the source supports one.
- For claims about performance, cost, security, or reliability, either cite the
	supplied source, qualify the claim, or remove it. Avoid superlatives such as
	"best", "fastest", "always", and "never" unless they are verified guarantees.

## Source and accuracy behavior

- Treat supplied documentation, code, schemas, and links as the source of truth for product-specific claims.
- Do not invent commands, API fields, limits, pricing, version behavior, citations, or links.
- If the source is missing or uncertain, state the assumption or mark the detail for verification instead of presenting it as fact.
- Preserve version-specific and date-specific qualifications.
- When creating new technical documentation from a source, distinguish source-backed facts from proposed examples or recommendations.
- Treat examples as illustrative unless the source identifies them as tested or
	normative. Do not turn an example value, threshold, or workflow into a universal
	rule.
- When source material conflicts or is version-sensitive, preserve the qualification
	and identify what needs verification. Do not silently reconcile the conflict.

## Output contract

Before writing, infer or ask for the audience, documentation type, target format, and source material when they are not clear. For a large technical page, produce a structure that can support:

- A title and overview
- A contents-oriented heading hierarchy
- Conceptual explanation and decision guidance
- Examples, commands, or configuration snippets
- Tables or diagrams where useful
- Limitations, constraints, risks, compatibility, or troubleshooting where relevant
- Related links and next steps

Do not add sections merely to satisfy this list. Include each section only when it serves the reader or is supported by the source.

## Editing behavior

- Keep the original meaning unless the user asks for a change.
- Remove redundancy and filler.
- Smooth awkward transitions.
- Replace abstract wording with direct wording.
- Improve readability without sounding artificial or overly casual.
- Preserve technical precision and non-negotiable facts.
- Remove generic introductions such as "In this article" when they add no useful
	orientation. Replace them with the page's purpose or expected outcome.
- Replace vague transitions such as "as mentioned earlier" with a precise term or
	a descriptive cross-reference.

## Templates

- ./assets/documentation-template.md
- ./assets/explanation-template.md
- ./assets/notes-template.md

## Quality bar

The result should sound like a knowledgeable human wrote it: clear, honest, easy to read, respectful, accessible, and confident without sounding inflated. For product documentation, it should also be scannable, source-grounded, structurally complete, and neutral in tone.

Before finalizing a document, note, or explanation, check:

- Can the reader identify the feature, scope, and purpose from the opening?
- Is the main choice or recommendation easy to find?
- Does each heading describe the reader's question or task?
- Are facts, instructions, examples, recommendations, and warnings distinguishable?
- Are prerequisites, permissions, defaults, limits, risks, and compatibility covered
  when relevant?
- Can the reader run or adapt each example, and do they know what success looks like?
- Are claims qualified and traceable to the source?
- Are links selective and descriptive?
- Does the ending provide a useful next step without repeating the introduction?
