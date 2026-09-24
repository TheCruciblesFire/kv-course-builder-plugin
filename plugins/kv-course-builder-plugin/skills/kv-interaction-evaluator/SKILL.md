---
name: kv-interaction-evaluator
description: use this skill to evaluate whether lesson content, sermon-derived material, course sections, student packet material, devotional concepts, or teaching ideas should become an interactive learner activity. trigger when a user asks whether something should be interactive, needs an interaction recommendation, wants to avoid interaction-for-novelty drift, or needs help deciding between non-interactive teaching, light reflection, guided practice, or a primary interaction. use when learner objective, learner action, friction, tone risk, source material, and platform constraints need to be weighed. do not use to build full exercises, generate embed code, create LMS packages, or produce student packets, lessons, workbooks, slides, devotionals, or full interactive activities unless explicitly requested.
---

# KV Interaction Evaluator

## Purpose
Evaluate whether ministry teaching material should become an interactive learner activity. Give a bounded recommendation without building the full interaction.

This skill protects against two errors:

- interaction-for-novelty drift: turning content into activities merely because interactivity is available
- missed learner engagement: leaving content passive when learners need active observation, sorting, discernment, practice, reflection, or self-check

## Routing
Use this skill when the user provides or refers to material such as:

- course lesson sections
- sermon-derived teaching or response sections
- student packet sections
- devotional concepts
- Bible study material
- theological concepts
- learner objectives or proposed activities
- Mini Course Generator or platform interaction ideas

Pair with other Skills when needed:

- Use `kv-source-transparency-check` when source categories are unclear or an interaction would turn user notes, prior GPT synthesis, external sources, or knowledge-file material into learner-facing answer logic.
- Use `kv-passage-faithfulness-check` when a Scripture-based interaction would create correct/incorrect answers, interpretation prompts, theological claims, or application feedback that may outrun the passage.
- Use `kv-multi-asset-throttle` when the request asks for evaluation plus full activity, lesson, packet, workbook, slide deck, embed code, or LMS-ready output.
- Use `kv-scripture-formatting-check` when Scripture quotation, reference labels, CSB attribution, or Blue Letter Bible links need cleanup.

## Hard Boundaries
Do not:

- build the full activity by default
- create embed code, LMS packages, Mini Course Generator card sets, or implementation files
- create full lessons, student packets, workbooks, leader guides, devotionals, or slide decks
- treat interaction as automatically better than teaching, reflection, prayer, or discussion
- make solemn pastoral material feel like a game
- turn disputed or weakly supported interpretation into answer-key certainty
- let observation prompts preload interpretation
- invent source material or add theological claims not present in the source
- write as though final statements, answer options, or activity items were reviewed when they were only inferred from the prompt
- collapse Activity Selector, Exercise Builder, and Platform Packaging into this evaluation skill

## Workflow

### 1. Identify the source material
Name the source type, intended learner or audience, controlling passage or source if supplied, delivery context, and evaluation limits. If information is missing, proceed provisionally instead of inventing details.

When referring to example statements, claims, answer options, or activity items that were not actually supplied in final form, use conditional wording such as `if included`, `if this statement is used`, or `if the final list contains this claim`.

### 2. Identify the learner action
Determine what the learner would actually do. Favor interaction only when there is a real learner action such as:

- observe
- compare
- classify
- discern
- sequence
- choose
- reflect
- apply
- diagnose
- practice
- recall
- self-check

If the material is mainly proclamation, prayer, worship, testimony, pastoral encouragement, solemn warning, or complex explanation, interaction may be optional or inappropriate.

### 3. Identify learner friction
Ask what the learner needs help seeing, sorting, practicing, remembering, applying, or discerning. Interaction is stronger when the content contains real friction, such as:

- distinguishing similar ideas
- comparing a claim to textual support
- recognizing overreach
- seeing a passage movement or sequence
- applying a doctrine responsibly
- identifying false assumptions
- practicing a response or decision

If there is little friction, prefer teaching, summary, reflection, or discussion.

### 4. Check instructional value against novelty
Recommend interaction only when it clarifies, reinforces, diagnoses, practices, or deepens learning. Reject interaction when the primary gain is novelty, visual variety, or platform usage.

### 5. Check tone and sensitivity
Flag when interactivity could trivialize:

- repentance
- suffering
- grief
- confession
- conviction
- worship
- trauma-adjacent content
- sacred Scripture
- pastoral correction
- emotionally weighty application

For tone-sensitive material, recommend guided reflection, prayer, leader-guided discussion, or non-interactive teaching instead of game-like mechanics.

### 6. Check source and faithfulness risk
For Scripture-based or theological material, do not convert uncertain claims into answer-key certainty. Recommend `kv-passage-faithfulness-check` when an activity would require correct/incorrect feedback for interpretive claims, when observation and interpretation may blur, or when application could become moralistic, prosperity-framed, speculative, or forced.

Recommend `kv-source-transparency-check` when the source base is unclear or blended.

### 7. Choose a recommendation level
Use one of these decisions:

- **Yes - interaction recommended**: active processing is needed, learner friction is real, tone is suitable, and the activity can remain source-faithful.
- **Optional - interaction may help**: interaction could improve engagement, but reflection, discussion, or teaching could also work.
- **No - keep non-interactive**: interaction would trivialize the material, add novelty without learning value, or require unsupported answer logic.

Also assign recommendation strength: **Strong**, **Moderate**, or **Light**.

### 8. Recommend only a broad format
Name the best broad format without building the full activity. Valid formats include:

- guided observation
- reflection prompt
- self-check card
- sorting
- matching
- sequencing
- discernment scenario
- compare / contrast
- claim-support check
- response selection
- short written response
- group discussion
- leader-guided reflection
- no interaction; keep as teaching

When the evaluation concerns a course lesson, Mini Course Generator, student packet, or adult-learning context, include:

- estimated time
- complexity level: Low / Moderate / High
- adult micro-learning fit: Strong / Moderate / Weak

Use `references/interaction-decision-rubric.md` if the decision is difficult or borderline. Use `references/evaluation-template.md` for the standard output format.

### 9. Give a bounded build recommendation
State the next step without authorizing full activity production. For a Yes decision, say whether to proceed toward activity design, but keep the learner-facing build gated until required source checks, passage-faithfulness checks, statement lists, answer logic, or platform constraints are settled.

Use explicit language such as `Do not build the learner-facing activity yet` when any required input or quality check remains.

### 10. Final gate
Before delivering, verify:

- Did the response make a Yes / Optional / No recommendation?
- Did it identify learner action and learner friction?
- Did it check tone and sensitivity?
- Did it include estimated time, complexity level, and adult micro-learning fit when relevant?
- Did it use conditional wording for unsupplied example statements, answer options, or final activity items?
- Did it avoid building the full activity?
- Did it avoid embed code, LMS packaging, lessons, packets, and other downstream assets?
- Did it flag source transparency or passage faithfulness risks where needed?
- Did it tell the user not to build the learner-facing activity yet when source statements, categories, or answer logic still need review?

If any gate fails, revise before delivering.

## Output Discipline
Default output is one interaction evaluation. Keep the response short enough to support a decision. Do not produce full exercise copy, answer keys, facilitator notes, card scripts, embed code, packet content, lesson drafts, or student-facing assets unless the user explicitly asks for that later and the request is routed through the appropriate downstream workflow.
