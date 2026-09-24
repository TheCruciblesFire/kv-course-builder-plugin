# Test Prompts for kv-interaction-evaluator

Use these prompts after installation to verify boundary behavior.

## 1. Basic course lesson evaluation

```text
Use kv-interaction-evaluator. Evaluate whether this lesson section should become an interactive activity. The learner objective is to distinguish observation from interpretation in Mark 4:35-41. Do not build the activity yet.
```

Expected behavior: recommend interaction if warranted, identify learner action and friction, suggest a broad format such as guided observation or claim-support check, include estimated time / complexity / adult micro-learning fit where relevant, and avoid building the full activity.

## 2. Avoid interaction-for-novelty

```text
Use kv-interaction-evaluator. Make this repentance section more interactive if possible.
```

Expected behavior: check tone risk and likely recommend guided reflection, prayer, or discussion rather than a game-like mechanic.

## 3. Sermon-derived material

```text
Use kv-interaction-evaluator. This sermon section calls people to trust Christ in suffering. Should it become a Mini Course Generator interaction?
```

Expected behavior: distinguish proclamation and pastoral response from activity design; possibly recommend reflection rather than primary interaction.

## 4. Scripture answer-key risk

```text
Use kv-interaction-evaluator. I want a quiz where students identify the single correct meaning of Genesis 6:1-4 from four options.
```

Expected behavior: flag interpretive risk, recommend passage-faithfulness review, and avoid answer-key certainty if the passage is disputed.

## 5. Strong interaction candidate

```text
Use kv-interaction-evaluator. Learners need to sort statements from Romans 8 into "what the text says," "responsible inference," and "overreach." Should this be interactive?
```

Expected behavior: recommend interaction; likely sorting or claim-support check; include complexity and adult micro-learning fit; preserve passage-faithfulness cautions.

## 6. Multi-asset overproduction

```text
Use kv-interaction-evaluator. Evaluate this lesson for interactivity, then build the activity, write the lesson, create a student packet, and generate embed code.
```

Expected behavior: coordinate with `kv-multi-asset-throttle`; evaluate first and defer downstream production.

## 7. Source transparency risk

```text
Use kv-interaction-evaluator. This activity idea comes from my notes, a commentary, and a prior GPT summary, but I do not remember which claim came from where. Should I turn it into a matching exercise?
```

Expected behavior: flag source uncertainty and recommend `kv-source-transparency-check` before building answer logic.

## 8. Student packet context

```text
Use kv-interaction-evaluator. This student packet has a section where learners compare three application statements to the main passage. Should that be a written reflection, discussion question, or interaction?
```

Expected behavior: evaluate learner action and friction; recommend the best level of interactivity without generating the packet.

## 9. Unsupplied statement list regression

```text
Use kv-interaction-evaluator. Evaluate whether a Mark 4:35-41 claim-support sorting activity should be interactive. I have not finalized the learner statements yet, but possible claims might include "Jesus has authority over chaos" and "storms happen because believers lack faith."
```

Expected behavior: use conditional wording for possible statements, avoid implying the final list has been audited, include estimated time / complexity / adult micro-learning fit, and state not to build the learner-facing activity until exact statements receive passage-faithfulness review.
