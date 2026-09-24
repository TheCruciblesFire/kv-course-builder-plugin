---
name: kv-student-workbook-generator
description: use this skill to convert completed ministry teaching content into a student-facing workbook. trigger when a user asks to turn a completed lesson, bible study, discipleship module, devotional lesson, course lesson, or approved teaching source into a workbook, student packet, guided worksheet, or learner-facing response resource. use when source preservation, sectioning, learner prompts, response spaces, application, prayer/response, print usability, and student-facing clarity matter. do not use to create leader guides, sermon listening guides, full courses, new passage studies, devotionals, slide decks, interactive exercises, or workbook content from undeveloped source material unless explicitly requested.
---

# KV Student Workbook Generator

## Purpose
Convert approved ministry teaching content into a student-facing workbook while preserving the source material's biblical burden, structure, source boundaries, theological cautions, and learner-facing clarity.

This skill creates the workbook itself when the source is sufficiently developed. It does not create a leader guide, sermon listening guide, full course, devotional, slide deck, interactive activity, or new passage study unless explicitly requested.

## Routing
Use this skill when the user asks to convert completed or approved source material into:

- student workbook
- student packet
- learner-facing worksheet
- guided response resource
- workbook page from a completed lesson, Bible study, devotional lesson, discipleship module, or course lesson

If the request asks for several assets at once, use or recommend `kv-multi-asset-throttle` before producing multiple outputs. If the source content is thin or undeveloped, produce a workbook-readiness note rather than fabricating a full workbook.

## Coordinate With Other KV Skills

- Use `kv-source-transparency-check` when the workbook source blends Scripture, user notes, prior GPT output, knowledge files, external sources, or generated synthesis without clear disclosure.
- Use `kv-passage-faithfulness-check` when workbook prompts, applications, or theological claims may outrun the controlling passage.
- Use `kv-multi-asset-throttle` when the user asks for workbook plus leader guide, slides, devotional, interactive exercise, course, or other downstream assets.
- Use `kv-scripture-formatting-check` when Scripture quotations, summaries, CSB attribution, reference labels, or Blue Letter Bible links need final cleanup.
- Use `kv-interaction-evaluator` when a workbook prompt may need an interactive activity; do not build the activity unless separately requested.

## Hard Boundaries
Do not:

- include leader-only notes, facilitator answers, teaching scripts, or answer keys in the student workbook
- invent a workbook from a thin idea or undeveloped source
- add major new theological claims not present in or warranted by the source
- reshape the source burden into a new lesson aim
- turn inferred application into direct biblical command
- create a full course, devotional, slide deck, leader guide, sermon listening guide, interactive exercise, embed code, or LMS package
- overload students with too many prompts or generic reflection questions
- use fill-in-the-blank gimmicks where reflection, observation, or discussion would be stronger
- create excessive response lines inside tables; use the cell space itself when the response area is already in a table
- quote large Scripture blocks without checking formatting and permission needs

## Workflow

### 1. Identify the source base
Name the source type, controlling Scripture or teaching focus, supplied source material, named external sources if any, and audit limits. If the source base is unclear, state the uncertainty.

### 2. Check workbook readiness
Classify the material as one of:

- **Ready for workbook conversion**
- **Needs light source clarification**
- **Needs stronger source material first**
- **Needs passage-faithfulness check first**

If the source is too thin, do not fabricate the workbook. Give a short readiness note and the minimum source material needed.

### 3. Preserve the source burden
Identify the source's central teaching burden and preserve it. Do not create a new lesson aim that changes the source's main emphasis.

### 4. Select workbook structure
Use the default structure in `references/workbook-template.md` unless the user requests a compact worksheet or a specific format.

### 5. Convert into student-facing language
Make the content clear, direct, pastoral, and learner-facing. Simplify dense source material without flattening the meaning. Remove teacher-only commentary.

### 6. Add learner prompts
Use `references/prompt-guidelines.md`. Prompts must be source-connected, answerable, concrete, and proportionate. Avoid generic spirituality, moralism, emotional manipulation, or interpretive overreach.

### 7. Add response spaces
Use `references/formatting-rules.md`. Keep response areas clean and printable. Avoid long blank lines inside table cells.

### 8. Add application and prayer response
Application must remain tethered to the passage or source teaching. Prayer response should be simple, pastoral, and aligned with the workbook burden.

### 9. Final quality gate
Before delivering, verify:

- the output is student-facing only
- the source burden is preserved
- leader-only content is excluded
- unsupported theological expansion is avoided
- Scripture references and quotation labels are clear enough
- prompts are source-connected and not excessive
- response spaces are usable for print or digital use
- no unrequested downstream assets were created

## Default Output
Produce the workbook directly when source material is sufficient. Use `references/workbook-template.md` for the default and compact templates.

For thin or unclear source material, use this compact readiness format:

```markdown
# Workbook Readiness Note

**Readiness:** Ready / Needs light clarification / Needs stronger source material / Needs passage-faithfulness check first

**Reason:** ...

**Minimum needed before workbook generation:** ...

**Safe next step:** ...
```

## Test Prompts
Use the prompts in `references/test-prompts.md` after installation.
