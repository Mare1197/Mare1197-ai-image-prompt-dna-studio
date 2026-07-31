# Start Building the AI Image Prompt DNA Studio

Work in this repository as the primary product designer, UX architect, technical architect, and implementation builder.

Read `AGENTS.md` and `docs/specifications/00-PROJECT-INDEX.md` first. Treat the repository as a technology-neutral product specification. Do not assume that any framework, database, backend, hosting platform, component library, repository structure, or existing implementation is required.

## First deliverable: plan and design exploration
Before production implementation:

1. Inspect all relevant specifications and any existing code.
2. Produce a concise product and implementation plan covering major systems, dependencies, risks, data durability, performance, accessibility, testing, and delivery milestones.
3. Generate at least four genuinely different UI/UX concepts using any available design, prototyping, visualization, image-generation, UX, design-system, or accessibility skills and tools.
4. Make the concepts structurally different—not palette swaps. Vary information architecture, navigation, panel model, prompt-building flow, bank discovery, reference management, preview/history presentation, density, and responsive adaptation.
5. Show each concept visually when the available tools permit it. Include its key screens or workspace view, main user flow, strengths, tradeoffs, and how it prevents clutter.
6. Recommend one direction, but do not choose for me.
7. Stop and ask me to approve one concept or a hybrid before building the production UI.

Do not ask unrelated setup questions before showing the concepts. Make reasonable assumptions and state them.

## After design approval
After I approve a direction:

1. Select the complete technology stack and architecture yourself.
2. Explain the choices briefly in terms of maintainability, performance, local persistence, future provider integrations, deployment, and the project’s actual needs.
3. Record the approved design and architecture decisions.
4. Build the whole product in small, verifiable milestones.
5. Continue automatically through ordinary milestones without repeatedly asking permission.
6. Run relevant tests, repair regressions, and keep implementation records current.
7. Continue until every item in `docs/specifications/10-ACCEPTANCE-CRITERIA.md` is verified.

Ask me only when blocked by credentials, an unavailable external service, a destructive or irreversible action, a material safety issue, or a genuine unresolved contradiction.

## Non-negotiable experience requirements
- The app must feel fabulous, modern, visually refined, fast, and calm without clutter.
- Use progressive disclosure, clear hierarchy, excellent spacing, adaptable panels, accessible interaction, and useful loading/empty/error states.
- Prompt text, Prompt DNA, locks, selected tags, references, uploaded images, crops, weights, presets, workflow progress, notes, history, and result reviews must never disappear because of navigation, generation, refresh, errors, reconnects, crashes, or application updates.
- Preserve prompt-box text until the user explicitly clears or replaces it.
- Never clear reference images after generation or unrelated actions.
- Include autosave, visible save status, undo/redo, checkpoints, session recovery, durable reference storage, backup/restore, and import/export.
- Use appropriate caching and memory strategies, but never treat a cache as the only copy of user data.
- Keep startup and large projects responsive through appropriate lazy loading, code splitting, incremental bank loading, virtualization, progressive image loading, request deduplication, background work, debounced persistence, and resource cleanup—or equivalent techniques appropriate to the selected stack.

## Product rules
Follow all product, Prompt DNA, bank, character, monster, wardrobe, footwear, vehicle, wrap, livery, decal, history, reference, result-feedback, workflow, provider, and safety requirements in the specification files.

Only the active `CLEAN_RENDER_PROMPT` may be sent to a generation provider. Normal prompt entry must never trigger generation automatically. The universal Prompt DNA must remain independent of provider adapters.

Begin by reading the specifications, inspecting the repository, creating the plan, and presenting the distinct UI/UX concepts for approval.