# AI Image Prompt DNA Studio — Product Specification

This repository contains the product specifications, content-bank requirements, workflow rules, resilience requirements, and acceptance criteria for building the AI Image Prompt DNA Studio.

It intentionally does **not** prescribe a programming language, framework, database, backend, hosting provider, component library, or repository structure.

## Start here

For an AI builder:

1. Read `AGENTS.md`.
2. Read `docs/specifications/00-PROJECT-INDEX.md`.
3. Use `AI-BUILDER-START-PROMPT.md` as the starting instruction.

## Mandatory workflow

Before production implementation, the builder must:

1. Inspect the specifications and any existing code.
2. Create a product and implementation plan.
3. Generate at least four genuinely different UI/UX design concepts using available design and prototyping tools.
4. Present the concepts visually with flows, strengths, tradeoffs, responsive behavior, and clutter-prevention strategy.
5. Wait for the user to approve one concept or a hybrid.
6. Choose and document the complete technology stack and architecture only after design approval.
7. Build and verify the complete product without repeatedly asking for routine confirmation.

## Key quality requirements

- Modern, fabulous, premium, uncluttered UI
- Beginner-friendly with advanced depth through progressive disclosure
- Structured Prompt DNA rather than tag concatenation
- Durable autosave and session recovery
- Prompt text and references never cleared by unrelated actions
- Clear save, offline, conflict, and recovery states
- Fast loading through appropriate incremental loading, caching, image optimization, and memory management
- Full history, branching, references, presets, feedback, and provider-independent Prompt DNA
- Still-image prompting and generation only

## Specification map

See `docs/specifications/00-PROJECT-INDEX.md` for the authoritative reading order and document descriptions.

Completion requires evidence for every criterion in `docs/specifications/10-ACCEPTANCE-CRITERIA.md`.