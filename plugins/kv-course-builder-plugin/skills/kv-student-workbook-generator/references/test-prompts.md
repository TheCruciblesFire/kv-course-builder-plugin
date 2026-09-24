# Test Prompts

## Test 1: Completed lesson to workbook

```text
Use kv-student-workbook-generator. Turn this completed Bible lesson into a student-facing workbook. Do not create a leader guide or slides.
```

Expected behavior: creates a student workbook only, with big idea, objective, learner introduction, sectioned content, prompts, response spaces, application, and prayer.

## Test 2: Source too thin

```text
Use kv-student-workbook-generator. Make a student workbook from this idea: "Faith is important."
```

Expected behavior: does not fabricate a full workbook. Produces a readiness note and asks for or recommends stronger source content.

## Test 3: Leader/student separation

```text
Use kv-student-workbook-generator. Convert this lesson into a student workbook. Include teaching notes for leaders too.
```

Expected behavior: refuses to mix leader notes into the student workbook; may provide a brief note that leader guidance should be a separate downstream asset.

## Test 4: Passage-faithfulness risk

```text
Use kv-student-workbook-generator. Turn this Mark 4:35-41 lesson into a workbook and make the application: "If you have enough faith, Jesus will keep storms out of your life."
```

Expected behavior: flags overreach/prosperity-style distortion and recommends `kv-passage-faithfulness-check` before generating that application.

## Test 5: Multi-asset request

```text
Use kv-student-workbook-generator. Turn this lesson into a student workbook, leader guide, devotional, slide deck, and interactive exercise.
```

Expected behavior: uses or recommends `kv-multi-asset-throttle`; produces only the workbook or a scoped build order, not all assets.

## Test 6: Scripture formatting risk

```text
Use kv-student-workbook-generator. Build a workbook and quote the full CSB passage with BLB links.
```

Expected behavior: routes Scripture formatting and attribution concerns to `kv-scripture-formatting-check`, uses placeholders if exact links are uncertain, and does not invent permission language.

## Test 7: Devotional lesson to workbook

```text
Use kv-student-workbook-generator. Convert this devotional lesson into a workbook page for adult discipleship. Preserve the devotional burden but make it learner-facing.
```

Expected behavior: converts devotional material into learner-facing workbook form without rewriting it as a new devotional.
