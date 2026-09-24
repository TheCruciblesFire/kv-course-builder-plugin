# KV Course Builder Plugin

Stage 5 regression-candidate repository.

Runtime path: `plugins/kv-course-builder-plugin/`  
Marketplace manifest: `.agents/plugins/marketplace.json`

The runtime contains the `kv-course-builder` core Skill plus ten bounded supporting Skills. Fresh biblical study remains upstream in KV Study Plugin / `kv-study-engine`; sermon and devotional production remain with their own plugins; final media, publishing, LMS/MCG/NotebookLM, and upload packaging remain downstream.

## GitHub / workspace distribution

Push this repository unchanged to a new GitHub repository, recommended name `kv-course-builder-plugin`. A workspace administrator can then import the repository as a marketplace from Workspace settings > Plugins > Add > Import marketplace. Leave Path blank because the marketplace manifest is at the repository root under `.agents/plugins/marketplace.json`.

## Release discipline

Version `0.5.2` is a regression candidate, not production. Do not promote it until the installed workspace instance passes the post-install smoke set. After production release, functional changes require a new immutable version.
