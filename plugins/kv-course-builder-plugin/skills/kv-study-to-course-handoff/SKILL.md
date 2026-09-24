---
name: kv-study-to-course-handoff
description: use this skill to convert a kv study engine passage study, inductive study, sermon-prep output, or biblical study handoff into a clean kv course builder handoff. trigger when a user asks for a study-to-course handoff, course-prep handoff, curriculum handoff, lesson-planning handoff, or conversion from study material into course-ready direction. use when preserving source transparency, passage burden, interpretive cautions, theological boundaries, and textual support levels matters. do not use to create a full course, full lessons, student packets, leader guides, workbooks, slides, devotionals, or interactive exercises unless explicitly requested.
---

# KV Study to Course Handoff

## Purpose
Convert upstream Study Engine or study-prep material into a bounded Course Builder handoff. Preserve the controlling passage, central burden, source base, interpretive cautions, theological boundaries, and support levels while giving course-ready direction without producing the course.

This skill does not perform a fresh passage study, design a full course, draft lessons, or replace Course Builder's work. It prepares a reliable handoff from Study Engine material to Course Builder.

## Routing
Use this skill when the user provides or refers to one of these inputs:

- KV Study Engine passage study
- inductive Bible study output
- sermon-prep output that needs course adaptation
- biblical study handoff
- user notes or uploaded study material that need Course Builder direction
- source-controlled passage study that needs course-prep formatting

Pair with other Skills when needed:

- Use `kv-source-transparency-check` when source categories are unclear, blended, missing, or need a final source statement.
- Use `kv-passage-faithfulness-check` when a course aim, theological synthesis, application, framework, or learner outcome may outrun the passage.
- Use `kv-multi-asset-throttle` when the request asks for a course plus packets, leader guides, slides, devotionals, exercises, LMS modules, or other downstream assets.
- Use `kv-scripture-formatting-check` when Scripture quotations, reference labels, CSB attribution, or Blue Letter Bible links need final cleanup.

## Hard Boundaries
Do not:

- create a full course unless the user explicitly asks for one
- create full lessons, lesson scripts, student packets, leader guides, workbooks, slides, devotionals, interactive exercises, embed code, or LMS-ready modules unless explicitly requested
- convert the study into polished student-facing course content
- add new major theological claims not present in or warranted by the supplied study
- treat Study Engine synthesis as Scripture
- erase interpretive cautions, source limitations, or uncertainty markers
- convert application lanes into required learner outcomes without marking their support level
- import a course framework, discipleship system, or doctrinal theme that the passage does not warrant
- blend Study Engine and Course Builder roles into one undifferentiated process

## Workflow

### 1. Identify the controlling material
Name the controlling passage, source material, and intended receiving GPT or workflow. If the passage is not explicit, infer only when the supplied material clearly identifies it; otherwise mark it as `unspecified in supplied material`.

### 2. Extract the study burden
Identify the passage's central burden using the supplied Study Engine or study-prep material. Preserve the study's emphasis rather than inventing a new course thesis.

Use this distinction:

- **Passage burden**: what the text itself appears to press on the reader.
- **Course direction**: how Course Builder may organize learning around that burden.
- **Learner outcome**: what learners may understand, believe, practice, discern, or discuss as a result.
- **Application lane**: a downstream implication that must remain tethered to the passage.

### 3. Preserve source transparency
Carry forward the source base in concise form:

- primary biblical text
- immediate context
- user-supplied notes or study material
- knowledge-file or framework influence explicitly present in the supplied material
- external sources, if named
- original-language or background claims, if present
- generated synthesis or inference

Preserve named or cited sources from the Study Engine output when present, including source names, file names, commentary names, lexical tools, user-supplied documents, and citation notes. If no external sources are named, state: “No external sources were named in the supplied study material.” Do not invent sources. If the source base is unclear, include a caution and recommend `kv-source-transparency-check`.

### 4. Classify claim support
For major claims and course-ready directions, classify support using these labels:

- **Direct textual claim**: explicitly stated or clearly shown in the passage.
- **Strong contextual inference**: strongly warranted by context, genre, structure, or argument flow.
- **Responsible biblical-theological synthesis**: canonically responsible but not the main point of the local passage alone.
- **Course application lane**: usable course implication that must remain tethered to the passage.
- **Caution / do not overstate**: potentially true, but not safe to make controlling without more support.

### 5. Preserve cautions and boundaries
Carry forward any Study Engine cautions, including:

- interpretive uncertainty
- genre or context limitations
- original-language restraint
- background-claim limits
- framework-overreach concerns
- moralism, prosperity framing, therapeutic drift, or speculative theology risks
- gospel-connection boundaries
- learner-outcome overreach
- downstream asset boundaries

### 6. Build the handoff only
Use the template in `references/handoff-template.md`. Keep the handoff course-ready and bounded. Include possible course direction, learner outcomes, and lesson-level directions, not completed lessons or course assets.

### 7. Final gate
Before delivering, check:

- Does the handoff preserve the controlling passage and central burden?
- Are direct textual claims distinguished from inference, synthesis, and course application?
- Are source categories clear enough?
- Are cautions and theological boundaries preserved?
- Did the output avoid becoming a full course or lesson draft?
- Are downstream assets deferred unless explicitly requested?

If any gate fails, revise before delivering.

## Output Discipline
Default output should be one handoff document with concise sections. Do not include polished lesson drafts, student-facing workbook language, facilitator notes, slide cues, interactive activities, devotionals, embed code, or asset production unless requested.
