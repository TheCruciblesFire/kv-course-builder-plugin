# Installation Notes for kv-interaction-evaluator

1. Upload `skill.zip` through the ChatGPT Skills interface.
2. Confirm the installed Skill name is `kv-interaction-evaluator`.
3. Confirm the display name is `KV Interaction Evaluator`.
4. Run the test prompts in `references/test-prompts.md` before treating the Skill as production-ready.
5. Validate that the Skill produces an evaluation only, not a full activity, lesson, packet, or embed package.
6. Validate that course, Mini Course Generator, student packet, and adult-learning evaluations include estimated time, complexity level, and adult micro-learning fit when relevant.
7. Validate that examples inferred from incomplete input use conditional wording, such as `If included...`.
8. Validate that the Skill explicitly says not to build the learner-facing activity yet when statement lists, category labels, source basis, or answer logic still need checking.
9. Confirm coordination with:
   - `kv-source-transparency-check`
   - `kv-passage-faithfulness-check`
   - `kv-multi-asset-throttle`
   - `kv-scripture-formatting-check`
10. Do not build additional KV Skills until this Skill passes boundary and fidelity tests.

## Updated Regression Checks

After installation, verify that evaluations include conditional wording when final learner statements are not supplied, and that course / Mini Course Generator evaluations include estimated time, complexity level, and adult micro-learning fit.
