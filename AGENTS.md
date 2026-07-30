# AI Image Prompt DNA Studio — Codex Instructions

## Authority order
1. Existing working code and verified Phase 0–1 decisions.
2. `docs/specifications/00-PROJECT-INDEX.md`.
3. The phase-specific documents assigned by the index.
4. Current handoff documents in `docs/`.

When documents conflict, preserve working code unless it violates a hard requirement. Record the conflict and resolution in `docs/implementation-log.md`.

## Operating rules
- First review and verify the claimed Phase 0 and Phase 1 work. Do not redo correct work.
- Continue phase by phase until the complete application satisfies the acceptance criteria.
- Do not pause for routine design, naming, implementation, or library decisions. Choose the safest maintainable option and document it.
- Ask the user only when blocked by credentials, an irreversible/destructive action, an unavailable external service, an unresolved safety issue, or two materially different product directions that cannot coexist.
- Do not ask for confirmation between ordinary phases.
- Keep the database, bank datasets, Prompt DNA engine, prompt composer, provider adapters, and UI separate.
- Load only documents and files needed for the active phase. Never load all bank datasets for unrelated work.
- Run relevant tests after every phase and repair failures caused by the changes.
- Update the handoff documents after every phase.
- Never claim completion without verification evidence.

## Required handoff files
Maintain:
- `docs/current-state.md`
- `docs/architecture.md`
- `docs/data-model.md`
- `docs/implementation-log.md`
- `docs/known-issues.md`
- `docs/next-phase.md`
- `docs/testing.md`

## Hard product constraints
- Still-image prompt building and image generation only. No video-generation system.
- Supported adapters: ChatGPT Images and Nano Banana Pro. Do not add Imagen or Sora adapters.
- Prompt generation must be based on structured Prompt DNA, not naive tag concatenation.
- The latest active `CLEAN_RENDER_PROMPT` is the only prompt source sent to a provider.
- Normal prompt entry never automatically generates an image.
- Use positive visual reframing for critical constraints.
- Adult lingerie/fashion options apply only to clearly adult characters and remain non-explicit editorial styling.
- Never select, recommend, randomize, or generate thick-soled, platform, chunky, dad, wedge, heavy-lug, bulky hiking, or oversized-foam footwear.
- Human characters and monsters must remain distinct subjects.
- Preserve exact vehicle model, modifications, wrap, livery, decals, and placement when locked.
- Render all user-created content as untrusted text; do not inject raw HTML.
