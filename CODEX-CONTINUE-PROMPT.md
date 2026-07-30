# Continue Building AI Image Prompt DNA Studio

Work in the repository that already contains the AI Image Prompt DNA Studio implementation.

Read `AGENTS.md` and `docs/specifications/00-PROJECT-INDEX.md` first. Then read the existing handoff files: `docs/current-state.md`, `docs/architecture.md`, `docs/data-model.md`, `docs/implementation-log.md`, `docs/known-issues.md`, `docs/next-phase.md`, and `docs/testing.md` when present.

The user reports that Phase 0 and Phase 1 are finished. Do not trust that blindly and do not redo them automatically. Review the actual code, tests, commits and documentation against the Phase 0 and Phase 1 acceptance requirements. Preserve correct work, repair missing or incompatible pieces, and document the review.

After the review, continue implementing the project phase by phase from the first incomplete phase until the entire application satisfies `docs/specifications/10-ACCEPTANCE-CRITERIA.md`.

Operating rules:
- Continue through ordinary phases without asking me for confirmation.
- Do not ask unnecessary questions about naming, layout details, libraries, file organization or routine implementation choices. Make the most maintainable reasonable decision and document it.
- Ask only when blocked by credentials, an irreversible/destructive action, a material safety issue, an unavailable external service, or a genuine product contradiction that cannot be resolved from the specifications.
- Do not discard existing working implementation.
- Keep the database/persistence package separate from Prompt DNA, bank data, composer, provider adapters and UI.
- Keep large bank datasets split by category and loaded lazily. Do not load all banks into context for unrelated work.
- For each phase: inspect only relevant files, implement it fully, run tests, fix regressions, update all handoff documents and continue to the next phase.
- Use the specification index to limit context. Do not reread the full repository or all specification files every phase.
- Never introduce video generation, Sora/Imagen adapters, ComfyUI, node-first UI, sampler/scheduler/guidance controls, automatic generation, or thick-soled footwear.
- Preserve the exact active `CLEAN_RENDER_PROMPT` source rule and safe user-text rendering.
- Do not claim the project is finished until all acceptance criteria have been verified with evidence.

At each phase boundary update:
- `docs/current-state.md`
- `docs/architecture.md`
- `docs/data-model.md`
- `docs/implementation-log.md`
- `docs/known-issues.md`
- `docs/next-phase.md`
- `docs/testing.md`

Begin now by reviewing Phase 0 and Phase 1, state what is valid and what needs repair, perform those repairs, and then continue from the first incomplete phase. Do not stop merely to ask whether you should continue.
