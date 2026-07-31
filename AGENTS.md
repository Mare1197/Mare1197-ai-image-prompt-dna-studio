# AI Image Prompt DNA Studio — Builder Instructions

## Purpose
This repository is a product specification and workflow guide. It intentionally does not prescribe a programming language, framework, database, hosting platform, component library, or repository structure.

The builder must choose the complete technical approach after understanding the product and after the user approves a design direction.

## Authority order
1. `docs/specifications/00-PROJECT-INDEX.md`
2. Product and domain specifications referenced by the index
3. The user-approved design direction and recorded design decision
4. Verified implementation behavior and tests

Existing code may be reused when it satisfies the specifications, but it is not automatically authoritative. Do not preserve an implementation merely because it already exists.

## Mandatory builder workflow
1. Inspect the repository and read the specification index.
2. Produce a concise product, UX, architecture, risk, and delivery plan.
3. Create multiple genuinely different UI/UX design directions before production implementation.
4. Use any available design, prototyping, visualization, image-generation, UX-research, design-system, or accessibility skills and tools that improve the result.
5. Present the design directions to the user with visuals, key flows, strengths, tradeoffs, and responsive behavior.
6. Stop and obtain explicit user approval for one direction or a requested hybrid.
7. Only after approval, choose and document the full technology stack, architecture, data strategy, performance strategy, and deployment approach.
8. Build in small, verifiable milestones until every acceptance criterion is satisfied.

The required design approval is the only normal product checkpoint. After approval, continue without asking unnecessary questions. Ask only when blocked by credentials, an unavailable external service, a destructive or irreversible action, a material safety issue, or a genuine contradiction that cannot be resolved from the specifications.

## Design exploration rules
- Produce at least four substantially different concepts.
- Concepts must differ in information architecture, navigation, workspace organization, panel behavior, editing flow, reference handling, preview/history presentation, and responsive adaptation—not merely colors, fonts, or surface styling.
- At least one concept should optimize simplicity for beginners, one should optimize a powerful professional workspace, and one should explore a bolder but still practical interaction model.
- Preserve the product’s required capabilities while exploring different ways to expose them.
- Do not start full production implementation before the user approves a concept.

## Experience quality rules
The finished product must feel fabulous, modern, calm, fast, and intentional without becoming cramped or decorative at the expense of usability.

Use:
- Strong visual hierarchy
- Progressive disclosure
- Clear primary actions
- Resizable and adaptable work areas
- Consistent spacing and typography
- Accessible contrast and focus states
- Reduced-motion support
- Useful empty, loading, success, and error states
- Visual polish that supports the workflow rather than competing with it

## No-data-loss contract
User progress must not disappear because of navigation, generation, model changes, errors, refreshes, crashes, reconnects, or application updates.

At minimum:
- Autosave prompt drafts, Prompt DNA, locks, selections, presets, workflow progress, and review notes.
- Persist reference images, their roles, crops, weights, analysis, and relationships to versions.
- Preserve text in the prompt box until the user explicitly clears or replaces it.
- Never clear references after generation or an unrelated action.
- Provide visible save status, dirty-state indication, undo/redo, checkpoints, session recovery, and restore options.
- Separate temporary UI state from durable project state and document which data belongs to each.
- Treat in-memory caches as accelerators, never as the only copy of user work.

## Performance and resource rules
Choose technology-appropriate techniques that keep startup, search, editing, previews, and large histories responsive. Consider lazy loading, code splitting, incremental bank loading, virtualization, thumbnail/progressive image loading, safe caching, background processing, debounced saves, request deduplication, prefetching of likely next actions, and disciplined memory cleanup.

Do not load every bank, image, history item, or editor at startup. Avoid unnecessary rerenders, duplicate data, stale caches, retained object URLs, and unbounded memory growth. Performance improvements must never compromise persistence or correctness.

## Product architecture rules
- Keep presentation, durable data, Prompt DNA, bank content, prompt composition, compatibility rules, history, references, provider integrations, and result feedback logically separated.
- The exact architecture is the builder’s decision.
- Prompt generation must be based on structured Prompt DNA, not naive tag concatenation.
- The latest active `CLEAN_RENDER_PROMPT` is the only prompt source sent to a generation provider.
- Normal prompt entry never automatically generates an image.
- Provider integrations must not own or overwrite universal Prompt DNA.
- Render all user-created content as untrusted text; never inject raw user HTML.

## Hard product constraints
- Still-image prompt building and image generation only; no video-generation system.
- Supported adapters: ChatGPT Images and Nano Banana Pro. Do not add Imagen or Sora adapters.
- Use positive visual reframing for critical constraints.
- Adult lingerie and sensual fashion options apply only to clearly adult characters and remain non-explicit editorial styling.
- Never select, recommend, randomize, or generate thick-soled, platform, chunky, dad, wedge, heavy-lug, bulky hiking, oversized-foam, or otherwise elevated footwear.
- Human characters and monsters must remain distinct subjects unless the user explicitly requests a transformation concept.
- Preserve exact vehicle model, modifications, paint, wrap, livery, decals, and placement when locked.

## Required project records
Maintain concise, current records for:
- Product/build plan
- Approved design and rejected alternatives
- Architecture and technology decisions
- Data and recovery model
- Current implementation status
- Testing and verification
- Known limitations and issues

Never claim completion without evidence that the acceptance criteria were tested.