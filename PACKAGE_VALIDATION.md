# KV Course Builder Plugin — Stage 5 Package Validation

Build version: `0.5.1`  
Release state: NOT RELEASED  
Gate: package/static validation

## Result

PASS — ready for installed-instance regression testing.

## Deterministic checks
- Marketplace JSON parses.
- Portable plugin manifest JSON parses.
- Codex compatibility manifest JSON parses.
- Marketplace points to `./plugins/kv-course-builder-plugin`.
- Bundled Skill count: 11.
- All 11 bundled Skills pass the canonical quick validator.
- `kv-study-engine`, `kv-sermon-builder`, and `kv-devotion-builder` are not bundled.
- Core Course Builder references are bundled inside `kv-course-builder/references/`.
- No MCP server or custom Action is declared.
- Post-install smoke set is included.

This static PASS does not substitute for installed workspace smoke testing.
