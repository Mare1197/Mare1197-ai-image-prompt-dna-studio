# Phased Implementation and Context Strategy

## Before continuing
Review Phase 0 and Phase 1 instead of assuming they are correct. Compare code, tests and handoff documents against the requirements. Repair gaps without rewriting valid foundations.

## Phase 0 — Audit and architecture
Expected complete. Verify repository audit, package boundaries, database strategy, bank loading strategy, risks and handoff documents.

## Phase 1 — Shared types and Prompt DNA foundation
Expected complete. Verify schema versioning, validation, locks, change/exclusion/randomization states, diffs, serialization, migration and unit tests.

## Phase 2 — Database and persistence
Create framework-independent repositories and adapters: in-memory, structured local storage/IndexedDB, migrations, backup/restore, import/export and tests.

## Phase 3 — Bank schemas and loader
Create shared/specialized schemas, registry, lazy loaders, search/alias indexes, validation, user entries, favorites and import/export. Use small fixtures first.

## Phase 4 — Visual bank data
Populate styles, effects, combinations, locations, camera, lighting, palettes, moods and materials from separate category files.

## Phase 5 — Character, wardrobe and monster data
Populate adult human profiles, lingerie/fashion, skirts, heels, Vans and similar slim sneakers, poses, monsters and creature DNA. Enforce footwear restrictions.

## Phase 6 — Vehicle data
Populate approved car list, modification categories, wraps, liveries, decals, placements and vehicle presets.

## Phase 7 — Compatibility and positive-reframing engines
Build lock-aware conflict detection, auto-resolution, positive reframing, footwear enforcement, human/monster separation, vehicle consistency, camera conflicts and style-overload checks.

## Phase 8 — Prompt composer
Create stable coherent natural-language prompts from DNA. Separate universal prompt and provider adapters. No naive tag concatenation.

## Phase 9 — History and branching
Implement `0P`, `V1...`, named branches, active version, save/load/favorite/rate/notes/diff/restore/export.

## Phase 10 — Variation engine
Default bundle: Cinematic, Editorial, Camera, Lighting, Creative. Support scoped axes and preserve locks.

## Phase 11 — Reference engine
Multi-image upload, roles, priorities, focus regions, weights, locks and selective DNA extraction.

## Phase 12 — Application shell
Compact navigation, contextual resizable left panel, center workspace, no permanent right inspector, pinnable overlays, persistent layout and themes.

## Phase 13 — Prompt Architect workspace
Raw input, DNA extraction, rewrite, positive reframe, repair, active prompt, copy, save, variation and explicit generation controls.

## Phase 14 — Bank browsers/editors
Reusable modular browsers for every bank; search, filters, multi-select, locks, exclusions, favorites and user entries.

## Phase 15 — Presets and recipes
Partial presets, composition, import/export and lock-aware application.

## Phase 16 — Result review and learning
Structured evaluation, successful-field locking, minimal correction and linked next branch. Separate global/project/model lessons.

## Phase 17 — Generation history and previews
Batch rows, size slider, adaptive columns, enlarged viewer, thumbnails, keyboard loop, compare 2/4, prompt diff, notes and batch actions.

## Phase 18 — Workflows, approvals and audit
Editable workflows, pause/resume, approval queue, DNA/prompt diffs, undo/redo and audit records.

## Phase 19 — Provider adapters
ChatGPT Images and Nano Banana Pro only. App remains fully usable without credentials.

## Phase 20 — Integration and verification
Full tests, accessibility, responsive behavior, performance, safe rendering, backups, errors, docs, completed/pending report and known limitations.

## Continuous execution rule
Proceed from one verified phase to the next without asking for routine confirmation. Stop only for credentials, destructive/irreversible action, material product contradiction, safety issue or external blocker. Update handoff files after every phase.

## Phase completion output
Record completed work, changed files, decisions, tests, failures, migrations, exported interfaces, known issues and exact next phase. Do not partially mix unrelated phases.
