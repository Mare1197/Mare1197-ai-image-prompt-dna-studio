# Product Requirements

## Goal
Build a complete, polished AI Image Prompt DNA Studio for creating, rewriting, organizing, branching, adapting, reviewing, and generating still-image prompts. It must be beginner-friendly while supporting advanced structured control.

## Starting inputs
- Rough idea or fragments
- Existing prompt
- One or more reference images
- Saved prompt or version
- Saved character, monster, wardrobe, car, wrap, livery, or preset
- A style, effect, location, camera, lighting, or recipe
- A prior generated result

## Core capabilities
- Prompt creation, rewrite, polish, lint, score, repair and positive reframing
- Structured Prompt DNA editing
- Live prompt preview
- Exact/approximate locks, requested changes, exclusions and randomization
- Five-direction default variation bundle and custom variation axes
- Version tree and diffs
- Reference image roles
- Reusable characters and monsters
- Adult fashion and lingerie editorial options
- Modified vehicles, wraps, liveries and decals
- Presets and recipes
- Result feedback and linked next iterations
- ChatGPT Images and Nano Banana Pro adapters
- Prompt-only mode when no provider is connected
- Local persistence, backup, import and export
- Editable workflows, approval history, undo/redo and audit trail

## Prompt-first rule
Entering or rewriting a prompt never generates automatically. Generation requires an explicit action. Only the latest active `CLEAN_RENDER_PROMPT`, relevant references, output settings and provider-specific formatting may be sent to a provider.

## Positive reframing
Transform restrictions into direct visual instructions. Examples:
- “Do not change the car” → preserve exact model, generation, body shape, modifications, wheels, stance, paint, wrap, livery, decals and placement.
- “Do not merge subjects” → render every subject as a separate body and silhouette with an independent pose and position.
- “No thick soles” → use only flat, slim, traditionally proportioned sneaker soles or slim high heels.

## Adult fashion rule
Lingerie and sensual styling are available only for clearly adult characters. Keep treatment non-explicit, editorial, fashion-oriented and professionally styled.

## Hard footwear exclusion
Never allow platform, thick-soled, chunky, dad, wedge, heavy-lug, bulky hiking, oversized-foam or otherwise elevated/thick footwear. Enforce at bank validation, search, presets, randomization, compatibility, composition, linting and result review.

## Non-goals
- No video generation, video timeline or animation system
- No Sora or Imagen adapter
- No ComfyUI or node-first interface
- No sampler, scheduler, guidance, prompt-strength or reference-strength controls
- No automatic generation from ordinary prompt entry
- No reliance on consumer subscriptions as API credentials
