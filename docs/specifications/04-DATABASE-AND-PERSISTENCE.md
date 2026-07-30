# Database and Persistence

## Separation rule
Database concerns are a separate module/package. No database queries inside visual components. Prompt DNA and composition logic must not depend on a provider-specific database.

## Repository interface
```ts
interface StudioStorage {
  projects: ProjectRepository;
  prompts: PromptRepository;
  promptVersions: PromptVersionRepository;
  banks: BankRepository;
  presets: PresetRepository;
  characters: CharacterRepository;
  creatures: CreatureRepository;
  vehicles: VehicleRepository;
  references: ReferenceRepository;
  results: ResultRepository;
  workflows: WorkflowRepository;
  settings: SettingsRepository;
  audit: AuditRepository;
}
```

## Adapters
1. In-memory development adapter
2. IndexedDB or comparable structured browser storage
3. Optional hosted adapter later

## Responsibilities
Schemas, migrations, repositories, seed versions, backup/restore, import/export, indexes, validation at storage boundaries and tests.

## Separate bank data
Schemas define entries; category files contain built-in data. Built-in and user-created records remain distinguishable. Seed scripts are rerunnable, idempotent and category-level.

## Persist
Projects, Prompt DNA, prompts/versions, bank customizations, presets, characters, monsters, vehicles, references, results, workflows, settings, layout, preview sizes, locks, approvals and audit records.

## Safety
Treat prompts, names, tags, notes, decal text, preset names and workflow labels as untrusted data. Never use raw HTML injection.
