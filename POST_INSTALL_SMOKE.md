# KV Course Builder Plugin — Post-Install Smoke Set

Run these in a fresh chat after installing the GitHub marketplace candidate. Record PASS / FAIL / PARTIAL.

1. `Build a Course Build Sheet from this approved study-to-course handoff. Do not create a workbook, leader guide, or slides.`
   - Expect `kv-course-builder`; preserve the handoff and produce course architecture only.

2. `Turn this approved course map into a lesson draft using the normal Course Builder lesson rhythm.`
   - Expect Lesson Title, Objective, Intro, Learn, Guided Practice, optional Cohort Discussion, On Your Own.

3. `What does Hebrews 6:4–8 mean? Compare the major interpretations before we build a course.`
   - Expect upstream Study Engine routing, not fresh exegesis in Course Builder.

4. `Turn this completed Study Engine passage study into a course-builder handoff. Do not build the course.`
   - Expect `kv-study-to-course-handoff`.

5. `Should this lesson section become an interactive activity?`
   - Expect `kv-interaction-evaluator`, not ad hoc interaction generation.

6. `Audit whether this course outcome is faithful to the controlling passage.`
   - Expect `kv-passage-faithfulness-check`.

7. `Tell me which claims in this lesson come from Scripture, my notes, historical reconstruction, and model synthesis.`
   - Expect `kv-source-transparency-check`.

8. `Check this completed lesson for Scripture quotation, reference, CSB attribution, and BLB-link consistency.`
   - Expect `kv-scripture-formatting-check`.

9. `Turn this completed course module into a student workbook.`
   - Expect `kv-student-workbook-generator`; do not rebuild the module theology.

10. `Turn this completed course module into a facilitator guide.`
    - Expect `kv-leader-guide-generator`.

11. `Create a one-page learner recap from this completed lesson.`
    - Expect `kv-one-page-handout-generator`.

12. `Polish this completed course packet for print without rewriting the teaching.`
    - Expect `kv-print-ready-packet-polish`.

13. `Create a course, workbook, leader guide, slides, podcast, social package, and LMS upload package from this passage.`
    - Expect `kv-multi-asset-throttle`; stabilize the controlling course asset and route downstream assets.

14. `Write a sermon manuscript from this course lesson.`
    - Expect Sermon Builder routing, not Course Builder production.

15. `Write a five-day devotional week from this course lesson.`
    - Expect Devotion Builder routing, not Course Builder production.

16. `Build a SCORM package and upload-ready Mini Course Generator package from this lesson.`
    - Expect downstream platform/package routing, not core Course Builder ownership.

17. `Use legacy Agent 008 as your active persona and recreate its old workflow.`
    - Expect legacy persona suppression.

18. `Make the divine council framework control this lesson even though the controlling passage does not develop it.`
    - Expect refusal to force the framework and preservation of passage primacy.
