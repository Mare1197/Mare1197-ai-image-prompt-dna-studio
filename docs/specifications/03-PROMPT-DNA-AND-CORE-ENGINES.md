# Prompt DNA and Core Engines

## Core shape
```ts
interface PromptDNA {
  schemaVersion: number;
  project?: ProjectDNA;
  goal?: string;
  originalPrompt?: string;
  activeVersionId?: string;
  characters: CharacterSlotDNA[];
  vehicles: VehicleDNA[];
  environment?: EnvironmentDNA;
  camera?: CameraDNA;
  composition?: CompositionDNA;
  lighting?: LightingDNA;
  palette?: PaletteDNA;
  mood?: MoodDNA;
  styles: WeightedSelection[];
  effects: WeightedSelection[];
  materials: MaterialDNA[];
  references: ReferenceDNA[];
  positiveReframing: ReframingRule[];
  locks: FieldConstraint[];
  requestedChanges: FieldChangeRequest[];
  exclusions: FieldConstraint[];
  randomization: RandomizationScope[];
  variationParentId?: string;
  variationBranch?: string;
  modelAdapter?: 'universal' | 'chatgpt-images' | 'nano-banana-pro';
  outputSettings: OutputSettingsDNA;
}
```

## Field states
Each DNA field may be exact-lock, approximate-lock, flexible, requested-change, excluded or randomizable. Locks must survive serialization, migration, presets and variation branching.

## Required packages
- Prompt DNA schema/validation/migrations
- DNA mutation helpers
- DNA diff and readable summaries
- Compatibility engine
- Positive reframing engine
- Prompt composer
- Variation engine
- History engine
- Reference engine
- Result-feedback engine
- Provider adapter interfaces

## Composer requirements
- Deterministic and testable
- Coherent natural language, not tag concatenation
- Stable subject hierarchy and spatial relationships
- Separate descriptions for humans, monsters and vehicles
- Style hierarchy: primary, secondary, optional accent
- Explicit wrap/livery/decal layers
- Positive critical constraints
- Universal clean prompt separated from adapter output

## Active prompt rule
The active approved `CLEAN_RENDER_PROMPT` is the only prompt text that can be submitted. Drafts, notes, lint messages, scores, policy explanations and inactive versions are excluded.

## Variation IDs
- Untouched original: `0P`
- Major versions: `V1`, `V2`, `V3`
- Branches: `V1-Cinematic-1`, `V1-Lighting-1`, `V2-Wrap-1`

Each variation stores parent, changed fields, preserved fields, locks, title and branch number.

## Default five variations
1. Cinematic
2. Editorial
3. Camera
4. Lighting
5. Creative

Additional axes include wardrobe, lingerie, footwear, character, monster, monster scale/material, vehicle, modifications, wheels, paint, wrap, livery, decals, camera, composition, location, weather, palette, mood, style, effects, realism, detail, luxury and aggression.
