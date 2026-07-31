# Project Specification Index

## Project
AI Image Prompt DNA Studio

## Purpose of this repository
This repository contains technology-neutral product specifications, domain banks, workflow rules, experience requirements, and acceptance criteria for an AI builder.

It does not prescribe a framework, programming language, database, backend, component library, hosting platform, or repository structure. The builder chooses those after the user approves a design direction.

## Mandatory starting order
1. `AGENTS.md`
2. This index
3. `01-PRODUCT-REQUIREMENTS.md`
4. `02-BUILDER-WORKFLOW.md`
5. `05-UI-AND-WORKSPACE.md`
6. `11-EXPERIENCE-PERFORMANCE-AND-RECOVERY.md`
7. Only the domain specifications needed for the current planning or implementation milestone
8. `10-ACCEPTANCE-CRITERIA.md` for verification

## Mandatory design gate
Before production UI implementation, the builder must create at least four genuinely different UI/UX concepts using any available design and prototyping skills or tools. The concepts must vary layout, information architecture, interaction flow, panel behavior, bank discovery, reference handling, and preview/history presentation—not only colors.

The user must approve one concept or a hybrid before the builder chooses the final stack and begins production UI implementation.

## Specification files
- `01-PRODUCT-REQUIREMENTS.md` — authoritative product behavior, rules, and non-goals
- `02-BUILDER-WORKFLOW.md` — planning, design exploration, approval, architecture selection, build, and verification workflow
- `03-PROMPT-DNA-AND-CORE-ENGINES.md` — technology-neutral Prompt DNA and engine behavior
- `04-DATABASE-AND-PERSISTENCE.md` — durable data, backend boundaries, autosave, recovery, cache, backup, and synchronization requirements
- `05-UI-AND-WORKSPACE.md` — design exploration, workspace capabilities, interaction rules, and responsive behavior
- `06-VISUAL-BANKS.md` — styles, effects, environments, camera, lighting, color, mood, and materials
- `07-CHARACTERS-WARDROBE-MONSTERS.md` — adult characters, fashion, footwear rules, monsters, creatures, poses, and actions
- `08-VEHICLES-WRAPS-LIVERIES-DECALS.md` — approved car library and vehicle DNA
- `09-HISTORY-REFERENCES-RESULTS.md` — prompt history, reference durability, review, learning, and exports
- `10-ACCEPTANCE-CRITERIA.md` — definition of complete
- `11-EXPERIENCE-PERFORMANCE-AND-RECOVERY.md` — no-data-loss contract, caching, loading, memory, and failure behavior
- `AI-BUILDER-START-PROMPT.md` — copy-ready instruction for the next AI builder

## Authority and decision rules
- Product behavior and hard constraints come from these specifications.
- Design structure comes from the user-approved design direction.
- The builder chooses technology and architecture only after design approval.
- Existing code may be reused, revised, or replaced according to quality and specification fit.
- Routine implementation decisions should not be escalated to the user.
- The builder should ask only for the required design approval or a genuine blocker.

## Context-window rule
Do not load the entire specification, every bank, image history, persistence implementation, and UI at once. Read this index, the current project records, and only the documents needed for the active planning or build milestone. Split large bank data by category and load it incrementally.