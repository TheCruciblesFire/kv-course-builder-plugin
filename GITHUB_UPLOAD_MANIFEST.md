# GitHub Upload Manifest

Recommended repository: `TheCruciblesFire/kv-course-builder-plugin`

Upload the entire contents of this repository ZIP without adding an extra parent folder.

Required root items:
- `.agents/`
- `plugins/`
- `docs/`
- `README.md`
- `POST_INSTALL_SMOKE.md`
- `NO_MCP_DECLARATION.md`
- `GITHUB_UPLOAD_MANIFEST.md`
- `PACKAGE_VALIDATION.md`

Marketplace import settings after commit:
- Source: `https://github.com/TheCruciblesFire/kv-course-builder-plugin`
- Path: leave blank
- Branch: `main` (or leave blank to use the default branch)

The marketplace manifest must resolve at `.agents/plugins/marketplace.json` and the plugin runtime at `plugins/kv-course-builder-plugin/`.
