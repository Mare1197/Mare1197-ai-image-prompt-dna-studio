# Product Requirements

## Goal
Create a complete, polished AI Image Prompt DNA Studio for creating, rewriting, organizing, branching, adapting, reviewing, and generating still-image prompts. It must be approachable for beginners while supporting advanced structured control.

The product must feel modern, fabulous, visually refined, uncluttered, fast, resilient, and trustworthy.

## Technology-neutral requirement
These specifications define outcomes and behavior, not a required stack. After the user approves a UI/UX design direction, the builder chooses the complete frontend, backend, data, hosting, testing, and deployment approach according to the product’s needs.

## Required design exploration
Before production UI implementation, create at least four genuinely different design concepts. They must vary information architecture and interaction—not only palette or styling. Present visuals, flows, strengths, tradeoffs, responsive behavior, and a recommendation. Wait for explicit user approval of a concept or hybrid.

## Starting inputs
- Rough idea or fragments
- Existing prompt
- One or more reference images
- Saved prompt or version
- Saved character, monster, wardrobe, car, wrap, livery, or preset
- A style, effect, location, camera, lighting, or recipe
- A prior generated result

## Core capabilities
- Prompt creation, rewrite, polish, lint, score, repair, and positive reframing
- Structured Prompt DNA editing
- Live prompt preview
- Exact and approximate locks, requested changes, exclusions, and randomization
- Five-direction default variation bundle and custom variation axes
- Version tree and diffs
- Reference-image roles and durable reference storage
- Reusable characters and monsters
- Adult fashion and lingerie editorial options
- Modified vehicles, wraps, liveries, and decals
- Presets and recipes
- Result feedback and linked next iterations
- ChatGPT Images and Nano Banana Pro adapters
- Prompt-only mode when no provider is connected
- Durable local progress, backup, import, export, and recovery
- Editable workflows, approval history, undo/redo, checkpoints, and audit trail

## Prompt-first rule
Entering or rewriting a prompt never generates automatically. Generation requires an explicit action. Only the latest active `CLEAN_RENDER_PROMPT`, relevant references, output settings, and provider-specific formatting may be sent to a provider.

## No-data-loss product rule
The application must preserve user work through navigation, model switching, generation, provider failure, validation errors, refreshes, reconnects, crashes, restarts, and application updates.

This includes:
- Prompt-box text and drafts
- Prompt DNA
- Selected, locked, excluded, and randomized tags
- Reference images, roles, crops, weights, focus areas, and notes
- Character, monster, vehicle, wrap, livery, and decal edits
- Presets and workflows
- Version history and result reviews
- Layout and workspace state

The application must provide autosave, visible save status, undo/redo, recoverable checkpoints, session restoration, backup/restore, and import/export. Unrelated actions must never silently clear a prompt or reference image.

## Performance product rule
The application must remain responsive with large banks, multiple references, extensive histories, and image batches. Load only what is needed, show progressive feedback, avoid blocking interactions, and manage cache and memory safely. Performance optimizations must never risk losing durable work.

## Positive reframing
Transform restrictions into direct visual instructions. Examples:
- “Do not change the car” → preserve exact model, generation, body shape, modifications, wheels, stance, paint, wrap, livery, decals, and placement.
- “Do not merge subjects” → render every subject as a separate body and silhouette with an independent pose and position.
- “No thick soles” → use only flat, slim, traditionally proportioned sneaker soles or slim high heels.

## Adult fashion rule
Lingerie and sensual styling are available only for clearly adult characters. Keep treatment non-explicit, editorial, fashion-oriented, and professionally styled.

## Hard footwear exclusion
Never allow platform, thick-soled, chunky, dad, wedge, heavy-lug, bulky hiking, oversized-foam, or otherwise elevated footwear. Enforce this in bank validation, search, presets, randomization, compatibility, composition, linting, and result review.

## Non-goals
- No video generation, video timeline, or animation system
- No Sora or Imagen adapter
- No ComfyUI or node-first interface
- No sampler, scheduler, guidance, prompt-strength, or reference-strength controls
- No automatic generation from ordinary prompt entry
- No reliance on consumer subscriptions as API credentials
- No technology stack mandated by this specification