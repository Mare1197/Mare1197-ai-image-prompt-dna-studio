# AI Image Prompt DNA Studio — Builder Instructions

## Purpose
This repository is a technology-neutral product specification and workflow control point. It does not prescribe a programming language, framework, database, hosting platform, component library, or implementation repository structure.

The intended repository name is:

`Mare1197/Mare1197-ai-image-prompt-dna-studio-instructions`

The builder chooses the complete technical approach only after understanding the product and after the user approves a design direction.

## Absolute `main` protection
Treat `main` as an immutable specification and control branch.

An AI builder must never independently:
- Commit or push design or implementation work to `main`
- Rewrite, reset, rebase, squash, force-push, delete, replace, repoint, or merge into `main`
- Interpret “build,” “continue,” “fix,” or “finish” as permission to alter `main`

Before any design or implementation write, inspect the repository, remotes, branch, and working tree. If the current branch is `main`, create and switch to a new branch or create a separate implementation repository.

Use branch names in this format:

`<project-or-design-name>--<ai-model>--<harness>`

Examples:
- `prompt-dna-studio--gpt-5-6--codex`
- `professional-workspace--claude-sonnet--claude-code`
- `approved-hybrid-ui--gemini-pro--antigravity`

Use lowercase, filesystem-safe slugs and record the full model and harness names in project records.

A separate implementation repository must also keep its default branch as a clean control point and begin generated work on a correctly named branch.

The builder may fetch, compare with, or restore context from `main` at any time. Only an explicit instruction naming `main` and the exact intended specification change authorizes a direct specification edit.

See `docs/specifications/12-BRANCH-SAFETY-AND-VISUAL-EVIDENCE.md` for the complete rules.

## Authority order
1. `docs/specifications/00-PROJECT-INDEX.md`
2. Product and domain specifications referenced by the index
3. The user-approved design direction and recorded design decision
4. Verified implementation behavior and tests

Existing code may be reused when it satisfies the specifications, but it is not automatically authoritative.

## Mandatory builder workflow
1. Inspect the repository, branch, remotes, existing implementation, and specification index.
2. Create or switch to the correctly named non-`main` branch before writing design or implementation files.
3. Use the highest reasoning effort available to analyze the product, architecture, UX, risks, persistence, performance, accessibility, security, and delivery strategy.
4. Produce a concise product, UX, architecture, risk, and delivery plan.
5. Actively provide suggestions, improvements, alternatives, simplifications, risks, and opportunities. Do not merely restate the requested steps.
6. Separate meaningful suggestions into **Recommended**, **Optional**, and **Experimental**, with benefit and tradeoff.
7. Create at least four genuinely different UI/UX directions before production implementation.
8. Use any available design, prototyping, visualization, image-generation, UX-research, design-system, testing, or accessibility skills that improve the result.
9. Save all visual design outputs in `design images/` on the active branch or implementation repository.
10. Present the concepts with visuals, key flows, strengths, tradeoffs, responsive behavior, clutter prevention, and a recommendation.
11. Stop for explicit approval of one concept, a hybrid, or requested revisions.
12. Only after approval, choose and document the complete stack, architecture, data strategy, performance strategy, testing approach, and deployment plan.
13. Prove one complete end-to-end vertical slice before scaling the build.
14. Continue through verifiable milestones without asking routine questions.
15. Capture actual screenshots of the running finished application before claiming completion.

The design approval is the only normal product checkpoint. Ask additional questions only for credentials, unavailable external services, destructive or irreversible actions, material safety issues, or a genuine unresolved contradiction.

## Higher-reasoning requirement
For complex UX, architecture, state, persistence, cache, concurrency, provider, and security decisions:
- Use the highest reasoning effort available in the active model or harness.
- Inspect evidence before deciding.
- Compare alternatives and tradeoffs.
- Identify edge cases, failure modes, and hidden dependencies.
- Challenge weak assumptions instead of rushing into code.
- Verify decisions with tests, visual inspection, and realistic scenarios.
- Record concise decisions and rationale without exposing private chain-of-thought.

## Planning and suggestions
During planning, identify:
- Missing user flows and hidden product gaps
- Clutter and discoverability risks
- State-loss, autosave, cache, memory, and synchronization risks
- Better interaction and information-architecture options
- Features that can be combined, deferred, simplified, or made safer
- Useful additions that materially improve the product without bloating it
- Better testing, recovery, and verification methods

Never silently remove a hard requirement. Optional or experimental suggestions that materially change the product require user approval.

## Design exploration
- Produce at least four structurally different concepts, not palette swaps.
- Vary information architecture, navigation, workspace organization, panels, prompt flow, Prompt DNA visibility, bank browsing, references, history, previews, responsive behavior, and beginner/expert density.
- Include at least one beginner-first concept, one professional high-density concept, and one distinctive but practical interaction model.
- Save concept images in `design images/concepts/<concept-name>/`.
- Save the approved or hybrid design in `design images/approved-design/`.
- Do not begin production UI implementation before approval.

## Highest-quality image requirement
Use the highest-quality practical images for design concepts and the implemented UI.

- Prefer high-resolution, crisp, professionally composed, legally usable, user-provided, or newly generated assets.
- Do not use blurry, visibly compressed, distorted, low-detail, stretched, or placeholder-like images when better assets are available.
- Preserve original high-quality sources separately from optimized delivery variants.
- Use thumbnails, responsive derivatives, modern formats, progressive loading, and lazy loading to preserve performance.
- Do not keep every full-resolution image decoded in memory.
- Visual quality must enhance the workflow without creating clutter.

## Required visual deliverables
Every design/build branch or implementation repository must contain:

```text
design images/
├── README.md
├── concepts/
├── approved-design/
└── final-screenshots/
```

Before completion, `design images/final-screenshots/` must contain actual screenshots from the running application, including where applicable:
- Main Prompt Architect workspace and populated main page
- Panels, pinned panels, pop-ups, menus, dialogs, drawers, overlays, and layovers
- Image editing mode
- References and Prompt DNA editing
- Character, monster, and vehicle workspaces
- Style, effect, wardrobe, vehicle, wrap, livery, and decal browsers
- History, branching, comparisons, and enlarged viewer
- Different workspaces and layouts
- Settings, provider connections, backup, recovery, and accessibility controls
- Tablet or narrow-screen layouts
- Loading, empty, save, offline, conflict, error, retry, and recovery states

These must be screenshots of the real implementation, not concept mockups. Include an indexed `design images/README.md` identifying every image and state.

## No login or welcome surfaces
Do not create login, sign-up, account-creation, authentication-gate, welcome, marketing landing, onboarding-carousel, splash, or mandatory setup-wizard pages.

Open directly into the usable main workspace. Optional contextual hints must be dismissible, non-blocking, remembered after dismissal, and must never erase work.

## Experience quality
The finished product must feel fabulous, modern, calm, fast, premium, and intentional without becoming cramped or decorative at the expense of usability.

Use strong hierarchy, progressive disclosure, clear actions, resizable work areas, excellent spacing and typography, accessible contrast, visible focus, reduced motion, and useful loading, empty, success, offline, conflict, error, and recovery states.

## No-data-loss contract
User progress must not disappear because of navigation, generation, model changes, errors, refreshes, crashes, reconnects, or updates.

At minimum:
- Autosave prompt drafts, Prompt DNA, locks, selections, presets, workflow progress, and review notes.
- Persist reference images, roles, crops, weights, analysis, and version relationships.
- Preserve prompt-box text until explicitly cleared or replaced.
- Never clear references after generation or unrelated actions.
- Provide save status, dirty-state indication, undo/redo, checkpoints, session recovery, backup, restore, import, and export.
- Separate temporary UI state from durable project state.
- Treat caches as accelerators, never the only copy of user work.

## Performance and resources
Choose stack-appropriate techniques for fast startup and stable long sessions, including lazy loading, code splitting, incremental banks, virtualization, progressive images, safe caching, background work, debounced saves, request deduplication, prefetching, cancellation, and memory cleanup.

Do not load every bank, image, history item, or editor at startup. Avoid stale caches, duplicate data, unnecessary rerenders, retained object URLs, and unbounded memory growth.

## Product architecture
- Keep presentation, durable data, Prompt DNA, bank content, composition, compatibility, history, references, providers, and result feedback logically separated.
- Prompt generation must use structured Prompt DNA, not naive tag concatenation.
- Only the latest active `CLEAN_RENDER_PROMPT` may be sent to a provider.
- Ordinary prompt entry never generates automatically.
- Provider adapters must not own or overwrite universal Prompt DNA.
- Treat all user-created content as untrusted text; never inject raw user HTML.

## Hard constraints
- Still-image prompt building and image generation only; no video-generation system.
- Supported adapters: ChatGPT Images and Nano Banana Pro only.
- Use positive visual reframing for critical constraints.
- Adult lingerie and sensual fashion options apply only to clearly adult characters and remain non-explicit editorial styling.
- Never select, recommend, randomize, or generate thick-soled, platform, chunky, dad, wedge, heavy-lug, bulky hiking, oversized-foam, or otherwise elevated footwear.
- Human characters and monsters remain distinct unless an explicit transformation is requested.
- Preserve exact vehicle model, modifications, paint, wrap, livery, decals, and placement when locked.

## Required records
Maintain concise current records for:
- Branch/repository identity, AI model, and harness
- Product/build plan and builder suggestions
- Approved design and rejected alternatives
- Architecture and technology decisions
- Data and recovery model
- Implementation status
- Testing and verification
- Known limitations and issues
- Design-image and final-screenshot index

Never claim completion without evidence for every acceptance criterion.