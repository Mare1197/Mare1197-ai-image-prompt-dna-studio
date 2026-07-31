# AI Image Prompt DNA Studio — Instructions

**Intended repository name:**

`Mare1197/Mare1197-ai-image-prompt-dna-studio-instructions`

This repository contains the technology-neutral product specifications, content-bank requirements, workflow rules, resilience requirements, branch-safety policy, visual-delivery requirements, and acceptance criteria for building the AI Image Prompt DNA Studio.

It intentionally does **not** prescribe a programming language, framework, database, backend, hosting provider, component library, or implementation repository structure.

## Start here
1. Read `AGENTS.md`.
2. Read `docs/specifications/12-BRANCH-SAFETY-AND-VISUAL-EVIDENCE.md`.
3. Read `docs/specifications/00-PROJECT-INDEX.md`.
4. Use `AI-BUILDER-START-PROMPT.md`.

## `main` is a control point
AI builders must never independently design, implement, commit, push, rewrite, reset, rebase, force-push, or merge work on `main`.

Create a branch using:

`<project-or-design-name>--<ai-model>--<harness>`

or use a separate implementation repository whose default branch remains a clean control point.

## Mandatory workflow
Before production implementation, the builder must:
1. Protect `main` and create the correctly named branch.
2. Use the highest reasoning effort available.
3. Produce a plan with Recommended, Optional, and Experimental suggestions—not only a checklist.
4. Generate at least four genuinely different UI/UX concepts using available design and prototyping tools.
5. Save high-quality concept images in `design images/concepts/`.
6. Present the concepts with flows, strengths, tradeoffs, responsive behavior, and clutter-prevention strategy.
7. Wait for user approval of one concept or a hybrid.
8. Save the approved direction in `design images/approved-design/`.
9. Choose and document the complete technology stack and architecture after approval.
10. Prove the critical end-to-end workflow, then build and verify the complete product.
11. Capture actual screenshots of the running application in `design images/final-screenshots/`.

## Key quality requirements
- Fabulous, modern, premium, calm, and uncluttered UI
- Direct launch into the main workspace—no login, welcome, marketing, onboarding, or blocking setup pages
- Beginner-friendly with advanced depth through progressive disclosure
- Structured Prompt DNA rather than tag concatenation
- Durable autosave and session recovery
- Prompt text and references never cleared by unrelated actions
- Clear save, offline, conflict, failure, and recovery states
- Fast loading through incremental data loading, caching, image optimization, and memory management appropriate to the selected stack
- Highest-quality practical concept and UI imagery, with optimized derivatives for performance
- Full history, branching, references, presets, feedback, and provider-independent Prompt DNA
- Still-image prompting and generation only

## Visual deliverables
Every build branch or separate implementation repository must contain:

```text
design images/
├── README.md
├── concepts/
├── approved-design/
└── final-screenshots/
```

See `docs/specifications/12-BRANCH-SAFETY-AND-VISUAL-EVIDENCE.md` for the complete visual evidence requirements.

Completion requires evidence for every criterion in `docs/specifications/10-ACCEPTANCE-CRITERIA.md`.