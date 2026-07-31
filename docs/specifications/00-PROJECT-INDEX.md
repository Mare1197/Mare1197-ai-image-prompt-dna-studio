# Project Specification Index

## Project
AI Image Prompt DNA Studio

## Intended repository

`Mare1197/Mare1197-ai-image-prompt-dna-studio-instructions`

## Purpose
This repository contains technology-neutral product specifications, domain banks, workflow rules, experience requirements, branch-safety rules, visual-delivery requirements, and acceptance criteria for an AI builder.

It does not prescribe a framework, programming language, database, backend, component library, hosting platform, or implementation repository structure. The builder chooses these after the user approves a design direction.

## Mandatory starting order
1. `AGENTS.md`
2. `12-BRANCH-SAFETY-AND-VISUAL-EVIDENCE.md`
3. This index
4. `01-PRODUCT-REQUIREMENTS.md`
5. `02-BUILDER-WORKFLOW.md`
6. `05-UI-AND-WORKSPACE.md`
7. `11-EXPERIENCE-PERFORMANCE-AND-RECOVERY.md`
8. Only the domain specifications needed for the current planning or implementation milestone
9. `10-ACCEPTANCE-CRITERIA.md` for verification

## Mandatory branch gate
`main` is the stable specification and control point. Builders must not write design or implementation work directly to `main`.

Before writing, create or switch to:

`<project-or-design-name>--<ai-model>--<harness>`

A separate implementation repository must also preserve its default branch as a clean control point and use a correctly named work branch.

## Mandatory planning quality
Use the highest reasoning effort available. Planning must contain active suggestions, alternatives, risks, improvements, and simplification opportunities rather than only repeating the specification.

Group meaningful suggestions as Recommended, Optional, and Experimental with benefits and tradeoffs.

## Mandatory design gate
Before production UI implementation:
- Create at least four genuinely different UI/UX concepts.
- Use available design, prototyping, visualization, image-generation, UX, design-system, and accessibility skills.
- Use high-quality practical images.
- Save concepts in `design images/concepts/`.
- Obtain user approval.
- Save the approved or hybrid direction in `design images/approved-design/`.

The concepts must vary layout, information architecture, interaction, panel behavior, bank discovery, reference handling, history, and previews—not only colors.

## Mandatory final visual evidence
Before completion, capture actual screenshots from the running implementation and save them in `design images/final-screenshots/`.

Maintain `design images/README.md` as a visual index. Concept images must never be represented as screenshots of the completed application.

## Specification files
- `01-PRODUCT-REQUIREMENTS.md` — product behavior, rules, and non-goals
- `02-BUILDER-WORKFLOW.md` — planning, suggestions, design exploration, approval, architecture selection, build, and verification
- `03-PROMPT-DNA-AND-CORE-ENGINES.md` — Prompt DNA and engine behavior
- `04-DATABASE-AND-PERSISTENCE.md` — durable data, backend boundaries, autosave, recovery, cache, backup, and synchronization
- `05-UI-AND-WORKSPACE.md` — design exploration, direct-to-workspace launch, visual quality, workspace capabilities, and responsive behavior
- `06-VISUAL-BANKS.md` — styles, effects, environments, camera, lighting, color, mood, and materials
- `07-CHARACTERS-WARDROBE-MONSTERS.md` — adult characters, fashion, footwear rules, creatures, poses, and actions
- `08-VEHICLES-WRAPS-LIVERIES-DECALS.md` — approved car library and vehicle DNA
- `09-HISTORY-REFERENCES-RESULTS.md` — prompt history, references, review, learning, and exports
- `10-ACCEPTANCE-CRITERIA.md` — definition of complete
- `11-EXPERIENCE-PERFORMANCE-AND-RECOVERY.md` — no-data-loss, caching, loading, memory, and failures
- `12-BRANCH-SAFETY-AND-VISUAL-EVIDENCE.md` — protected `main`, branch naming, model/harness identity, design images, image quality, final screenshots, and no login/welcome surfaces
- `AI-BUILDER-START-PROMPT.md` — copy-ready instruction for the next AI builder

## Authority and decision rules
- Product behavior and hard constraints come from these specifications.
- Design structure comes from the user-approved design.
- Technology and architecture are chosen after design approval.
- Existing code may be reused, revised, or replaced according to quality and specification fit.
- Routine implementation decisions should not be escalated.
- Ask only for design approval or a genuine blocker.

## Context-window rule
Do not load the entire specification, every bank, image history, persistence implementation, and UI at once. Read this index, current project records, and only the documents needed for the active milestone. Split and load large data incrementally.