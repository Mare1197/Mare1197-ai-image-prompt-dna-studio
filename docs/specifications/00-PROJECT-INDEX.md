# Project Specification Index

## Project
AI Image Prompt DNA Studio

## Current assumption
The user reports Phase 0 and Phase 1 as completed. Codex must verify them against the repository and tests before continuing. Preserve valid implementation and repair incomplete or incompatible work.

## Read order
1. `AGENTS.md`
2. `docs/current-state.md`, `docs/architecture.md`, `docs/data-model.md`, `docs/next-phase.md` if present
3. This index
4. `01-PRODUCT-REQUIREMENTS.md`
5. `02-PHASED-IMPLEMENTATION.md`
6. Only the phase-specific specification files needed for the current phase

## Specification files
- `01-PRODUCT-REQUIREMENTS.md` — authoritative product behavior and non-goals
- `02-PHASED-IMPLEMENTATION.md` — phase sequence, context strategy, acceptance gates
- `03-PROMPT-DNA-AND-CORE-ENGINES.md` — data model, locks, diffs, composer, variation logic
- `04-DATABASE-AND-PERSISTENCE.md` — separate persistence architecture
- `05-UI-AND-WORKSPACE.md` — workspace layout and interactions
- `06-VISUAL-BANKS.md` — styles, effects, environments, camera, lighting, color, mood, materials
- `07-CHARACTERS-WARDROBE-MONSTERS.md` — adult character, fashion, footwear and creature banks
- `08-VEHICLES-WRAPS-LIVERIES-DECALS.md` — car library and vehicle DNA
- `09-HISTORY-REFERENCES-RESULTS.md` — prompt history, references, review and learning
- `10-ACCEPTANCE-CRITERIA.md` — definition of complete
- `CODEX-CONTINUE-PROMPT.md` — copy-ready continuation prompt

## Context-window rule
Never load the entire specification and all banks at once. Read the index and active handoff, then only the documents directly relevant to the phase. Bank data must be split by category and loaded lazily.
