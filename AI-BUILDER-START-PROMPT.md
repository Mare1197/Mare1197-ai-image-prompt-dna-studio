# Start Building the AI Image Prompt DNA Studio

Work as the primary product designer, UX architect, technical architect, and implementation builder.

The intended specification repository is:

`Mare1197/Mare1197-ai-image-prompt-dna-studio-instructions`

Read `AGENTS.md`, `docs/specifications/00-PROJECT-INDEX.md`, and `docs/specifications/12-BRANCH-SAFETY-AND-VISUAL-EVIDENCE.md` first.

Treat the repository as a technology-neutral product specification. Do not assume any framework, database, backend, hosting platform, component library, repository structure, or existing implementation is required.

## Before writing anything
1. Inspect the current repository, remotes, branch, and working tree.
2. Never design, implement, commit, push, rewrite, or merge work directly on `main`.
3. If currently on `main`, create and switch to a new branch named:

   `<project-or-design-name>--<ai-model>--<harness>`

4. Alternatively, create a separate implementation repository when explicitly requested or clearly safer, but keep its default branch as a clean control point and work on a correctly named branch.
5. Record the full AI model and harness used.

`main` may be read, fetched, compared, or used as a restore/control point. Do not modify it unless the user explicitly names `main` and specifies the exact intended specification change.

## First deliverable: thoughtful plan and design exploration
Use the highest reasoning effort available. Do not rush into code.

Before production implementation:
1. Inspect all relevant specifications and any existing code.
2. Produce a concise product and implementation plan covering major systems, dependencies, risks, durability, performance, cache, memory, accessibility, testing, and delivery milestones.
3. Provide active suggestions rather than merely repeating the requested steps.
4. Separate suggestions into:
   - **Recommended** — materially improve quality, usability, safety, or maintainability
   - **Optional** — useful but not required for the first complete version
   - **Experimental** — distinctive or higher-risk ideas requiring approval
5. Explain the benefit and tradeoff of each meaningful suggestion.
6. Generate at least four genuinely different UI/UX concepts using any available design, prototyping, visualization, image-generation, UX, design-system, and accessibility skills or tools.
7. Make the concepts structurally different—not palette swaps. Vary information architecture, navigation, panels, prompt-building flow, Prompt DNA visibility, bank discovery, reference handling, preview/history presentation, density, and responsive adaptation.
8. Save concept visuals in:

   `design images/concepts/<concept-name>/`

9. Use the highest-quality practical images available: crisp, high-resolution, professional, properly composed, and free from obvious distortion or compression artifacts.
10. Present each concept visually with key screens, main flow, strengths, tradeoffs, responsive behavior, accessibility, and clutter-prevention strategy.
11. Recommend a direction, but do not choose for the user.
12. Stop and obtain approval for one concept, a hybrid, or revisions before production UI implementation.

Do not ask unrelated setup questions before showing the concepts. Make reasonable assumptions and state them.

## After design approval
1. Save the approved or hybrid design in `design images/approved-design/`.
2. Choose the complete technology stack and architecture yourself.
3. Briefly justify choices using maintainability, performance, local persistence, future provider integrations, deployment, accessibility, and actual product needs.
4. Record the approved design, rejected alternatives, stack, architecture, data model, resilience strategy, and performance plan.
5. Prove one end-to-end vertical slice before expanding the whole application:
   - Enter and autosave a prompt
   - Edit Prompt DNA
   - Add and persist a reference
   - Create the clean prompt
   - Save a version
   - Reload or restart and restore everything
6. Repair weaknesses found in the vertical slice.
7. Build the complete product in small, verifiable milestones.
8. Continue automatically through routine milestones without repeatedly asking permission.
9. Run relevant tests, perform visual verification, repair regressions, and keep records current.
10. Continue until every item in `docs/specifications/10-ACCEPTANCE-CRITERIA.md` has evidence.

Ask only when blocked by credentials, an unavailable external service, a destructive or irreversible action, a material safety issue, or a genuine unresolved contradiction.

## Final visual delivery
Before claiming completion, run the application and save actual high-resolution screenshots in:

`design images/final-screenshots/`

Include realistic populated examples of:
- Main Prompt Architect workspace and main page
- Contextual and pinned panels
- Pop-ups, menus, dialogs, drawers, overlays, and layovers
- Image editing mode
- Reference-image workflow
- Prompt DNA editor
- Character, monster, and vehicle workspaces
- Style, effect, wardrobe, wrap, livery, and decal browsers
- History, branching, comparisons, and enlarged viewer
- Different workspaces or layouts
- Settings, provider connections, backup, recovery, and accessibility controls
- Tablet or narrow-screen adaptation
- Important loading, empty, save, offline, conflict, error, retry, and recovery states

These must be screenshots of the real implemented application, not design mockups. Add an index to `design images/README.md` identifying each image and state.

## No login or welcome pages
Do not create login, sign-up, account creation, authentication gates, welcome pages, marketing landing pages, onboarding carousels, blocking splash pages, or mandatory setup wizards.

Open directly into the usable main workspace. Contextual hints may be dismissible and non-blocking.

## Non-negotiable experience requirements
- Fabulous, modern, visually refined, fast, calm, and uncluttered
- Strong hierarchy, progressive disclosure, excellent spacing, adaptable panels, accessible interaction, and useful loading/empty/error/recovery states
- Prompt text, Prompt DNA, locks, tags, references, images, crops, weights, presets, workflow progress, notes, history, and reviews never disappear because of navigation, generation, refresh, errors, reconnects, crashes, or updates
- Prompt-box text remains until explicitly cleared or replaced
- References never clear after generation or unrelated actions
- Autosave, save status, undo/redo, checkpoints, session recovery, durable reference storage, backup/restore, and import/export
- Caches accelerate access but are never the only copy of user work
- Fast startup and large-project performance through stack-appropriate lazy loading, splitting, incremental banks, virtualization, progressive images, deduplication, background work, debounced persistence, cancellation, and memory cleanup
- Highest-quality practical UI imagery, with optimized derivatives for fast delivery

## Product rules
Follow every product, Prompt DNA, bank, character, monster, wardrobe, footwear, vehicle, wrap, livery, decal, history, reference, feedback, workflow, provider, resilience, branch, and safety requirement in the specifications.

Only the active `CLEAN_RENDER_PROMPT` may be sent to a generation provider. Ordinary prompt entry must never generate automatically. Universal Prompt DNA remains independent of provider adapters.

Begin by protecting `main`, creating the correctly named branch, reading the specifications, producing the plan with suggestions, and presenting the distinct visual UI/UX concepts for approval.