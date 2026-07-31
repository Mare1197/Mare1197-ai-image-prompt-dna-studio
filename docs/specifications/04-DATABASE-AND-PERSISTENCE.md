# Data, Backend, Persistence, Cache, and Recovery Requirements

## Technology-neutral rule
This document defines required behavior, boundaries, and recovery guarantees. It does not prescribe a database, backend, storage engine, synchronization service, API style, or deployment platform.

The builder chooses the data architecture after the user approves a design direction.

## Separation rule
Durable data behavior must remain logically separate from visual components and provider-specific prompt generation.

The presentation layer should request data through clear application-level boundaries rather than owning persistence rules. Prompt DNA and prompt composition must remain portable across storage or provider changes.

## Data domains
The chosen architecture must support durable records for:
- Projects and workspaces
- Prompt drafts and clean prompts
- Prompt DNA and schema/data versions
- Prompt versions, branches, diffs, and active state
- Built-in and user-created bank entries
- Presets and recipes
- Human characters
- Monsters and creatures
- Vehicles, modifications, wraps, liveries, and decals
- Reference images and all reference metadata
- Generated results and result reviews
- Workflows and workflow progress
- Settings, layout, panels, filters, themes, and preview sizes
- Approvals, checkpoints, undo history, and audit records

## No-data-loss contract
The source of truth for user work must be durable. Memory caches, component state, temporary files, and previews must never be the only copy.

Required behavior:
- Autosave prompt-box text and Prompt DNA after short, non-disruptive delays and at important boundaries such as blur, navigation, generation, and window close when possible.
- Preserve unsaved work during validation, provider requests, model switching, tab changes, route changes, and recoverable errors.
- Save reference images or durable references to them before dependent actions begin.
- Preserve reference roles, crops, weights, focus areas, analysis, and version relationships.
- Never clear prompt text, selected references, or current edits after an unrelated action.
- Restore the most recent recoverable session after a crash, restart, or interrupted update.
- Show whether work is saved, saving, unsaved, offline, conflicted, or failed to persist.
- Provide explicit clear/delete actions with confirmation for destructive operations.

## Checkpoints and recovery
Provide:
- Undo and redo for meaningful edits
- Automatic recovery checkpoints
- User-created snapshots or named versions
- Session recovery after abnormal termination
- Backup and restore
- Import and export
- Safe migration of older stored data
- Recovery from partially completed writes or interrupted uploads
- A clear path for resolving synchronization conflicts when multiple copies exist

## Cache requirements
Caching should make repeated navigation, bank search, thumbnails, previews, and histories faster, but it must not become the authoritative copy of user work.

The builder should define:
- What is safe to cache
- Cache lifetime and invalidation
- How stale data is detected
- How caches are rebuilt
- How offline or unavailable data is represented
- How cache failures avoid corrupting durable state

## Reference and image handling
- Original references must remain retrievable after reload and restart.
- Store enough metadata to reconnect every reference to its project, role, crop, analysis, prompt version, and result.
- Use efficient thumbnails and progressive loading for browsing.
- Avoid decoding or retaining every full-resolution image simultaneously.
- Release temporary resources when they are no longer needed.
- Upload, analysis, or generation failures must not remove the user’s original reference.
- Replacing or deleting a reference must be explicit and reversible when practical.

## Search and indexing
Search must cover banks, prompts, versions, characters, monsters, vehicles, presets, references, results, notes, tags, aliases, and relationships. Indexing must update safely as records change and must not block the primary editing workflow.

## Built-in and user-created data
Built-in bank data and user-created records must remain distinguishable. Updates to built-in data must not overwrite user customizations. Seed or initialization behavior must be repeatable without creating duplicates.

## Security and safe rendering
Treat prompts, names, tags, notes, decal text, preset names, workflow labels, imported files, and metadata as untrusted data.

- Do not inject raw user HTML.
- Validate imported data before applying it.
- Protect credentials and provider secrets.
- Avoid exposing private references or project data through logs, public URLs, or error messages.
- Use least-privilege access appropriate to the selected architecture.

## Verification
Test persistence under:
- Normal editing
- Rapid edits
- Navigation during save
- Refresh and restart
- Offline or interrupted connection
- Provider failure
- Upload failure
- Storage quota or backend error
- Schema/data migration
- Backup and restore
- Multiple open views or conflicting edits where supported