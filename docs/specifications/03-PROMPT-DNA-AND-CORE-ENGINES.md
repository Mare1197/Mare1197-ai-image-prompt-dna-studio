# Prompt DNA and Core Engine Requirements

## Purpose
Prompt DNA is the structured source of truth from which clean prompts, variations, history records, presets, compatibility checks, and provider-specific outputs are derived.

The builder chooses the implementation language, schema system, module structure, and validation approach.

## Conceptual Prompt DNA model
Prompt DNA must be able to represent:

- Project identity and goal
- Original user input
- Active prompt version
- Human characters
- Monsters and creatures
- Wardrobe and footwear
- Poses, actions, and spatial relationships
- Vehicles
- Vehicle modifications
- Wheels, paint, wraps, liveries, decals, and placements as independent layers
- Environment and location
- Camera and composition
- Lighting
- Palette and mood
- Styles with a clear hierarchy
- Effects and materials
- References and their assigned roles
- Positive reframing rules
- Locks and preservation levels
- Requested changes
- Exclusions
- Randomization scopes
- Variation parent and branch relationships
- Provider adapter selection
- Output settings
- Schema or data version for safe future migration

## Field states
Every relevant field may be:
- Locked exactly
- Locked approximately
- Flexible
- Requested to change
- Excluded
- Randomizable

These states must survive autosave, serialization, migration, presets, version branching, backup, restore, and application restart.

## Required engine behaviors
The system must provide:
- Prompt DNA validation and safe evolution over time
- Controlled mutations
- Human-readable summaries
- Field-level and version-level diffs
- Compatibility and conflict detection
- Positive reframing
- Coherent prompt composition
- Variation generation
- History and branching
- Reference assignment and selective extraction
- Result feedback and learning
- Provider adaptation without changing universal DNA

The builder may organize these capabilities however it considers most maintainable, provided their responsibilities remain clear and testable.

## Composer requirements
- Produce coherent natural language, not a raw concatenation of tags.
- Preserve stable subject hierarchy and spatial relationships.
- Describe humans, monsters, and vehicles as distinct subjects.
- Use a clear style hierarchy: primary, secondary, and optional accent.
- Keep paint, wrap, livery, and decal descriptions independent.
- Convert critical restrictions into positive visual instructions.
- Produce a universal clean prompt separately from provider-specific output.
- Produce predictable results for the same DNA and clearly explain meaningful changes.

## Active prompt rule
The latest active and approved `CLEAN_RENDER_PROMPT` is the only prompt text that may be submitted to a provider. Drafts, notes, lint messages, scores, policy explanations, rewrite commentary, and inactive versions must not be included.

## History identifiers
- Untouched original: `0P`
- Major versions: `V1`, `V2`, `V3`
- Branches: descriptive parent-based IDs such as `V1-Cinematic-1`, `V1-Lighting-1`, or `V2-Wrap-1`

Each variation stores its parent, changed fields, preserved fields, locks, title, and branch sequence.

## Default five variations
1. Cinematic
2. Editorial
3. Camera
4. Lighting
5. Creative

Additional axes include wardrobe, lingerie, footwear, character, monster, monster scale or material, vehicle, modifications, wheels, paint, wrap, livery, decals, camera, composition, location, weather, palette, mood, style, effects, realism, detail, luxury, and aggression.

## Durability requirements
Prompt DNA changes must be recoverable. Editing, validation, generation, provider errors, route changes, or application restart must not discard the active DNA or draft. Maintain a recoverable change history and visible persistence state.