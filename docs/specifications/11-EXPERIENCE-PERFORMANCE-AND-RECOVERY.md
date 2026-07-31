# Experience, Performance, Cache, Memory, and Recovery

## Purpose
This document defines experience-quality and resilience outcomes. The builder chooses the technologies and implementation techniques.

## No-data-loss contract
The product must protect user work by default.

Classify every meaningful state as one of:
- Temporary presentation state
- Recoverable session state
- Durable project state
- Versioned history or audit state

Document the classification and persistence behavior for each major feature.

Durable or recoverable state includes:
- Prompt-box text and drafts
- Prompt DNA and constraints
- Active version and branches
- Reference images and metadata
- Upload and analysis progress
- Bank selections and custom entries
- Characters, monsters, vehicles, wraps, liveries, and decals
- Presets and workflows
- Generated results and result reviews
- Layout and workspace preferences

## Autosave behavior
- Save unobtrusively after meaningful edits using an appropriate delay.
- Save at risk boundaries such as navigation, generation, model changes, project switching, and close or suspend events when possible.
- Coalesce rapid changes without losing the most recent state.
- Show clear states such as Saved, Saving, Unsaved, Offline, Conflict, and Save failed.
- Retry recoverable failures without blocking continued editing.
- Never replace a newer local edit with an older asynchronous response.

## Recovery behavior
Provide:
- Undo and redo
- Automatic checkpoints
- Named snapshots or versions
- Restore of the last recoverable session
- Recovery after abnormal termination
- Backup and restore
- Import and export
- Safe data migrations
- Conflict detection and understandable resolution

The user should be able to recover from accidental replacement, deletion, failed generation, interrupted upload, or corrupted session without losing the entire project.

## Reference-image resilience
- Persist references before analysis or generation depends on them.
- Keep originals or durable retrievable copies separate from thumbnails and caches.
- Preserve roles, crops, focus, weights, notes, analysis, and version relationships.
- Keep failed or incomplete uploads visible with retry and replacement actions.
- Do not clear references after generation, navigation, provider errors, or model changes.
- Release temporary previews without deleting durable references.

## Performance goals
The product should feel immediate during common actions and remain stable with large projects.

The builder should establish measurable targets for:
- Initial usable screen
- Prompt typing and DNA updates
- Bank search and filtering
- Panel opening and navigation
- Draft autosave
- Thumbnail and preview appearance
- History scrolling and comparison
- Large project restoration

Targets may vary by platform, but slow operations must show progress and must not freeze the primary editor.

## Loading strategy
Use platform-appropriate approaches such as:
- Loading only the current workspace and required bank categories
- Splitting heavy features so they load when needed
- Incremental and paginated data retrieval
- Virtualizing long bank, history, and result collections
- Progressive thumbnails before full images
- Prefetching likely next views without loading everything
- Moving expensive parsing, indexing, image processing, or comparison work away from the main interaction path when possible

## Cache strategy
Define caches for appropriate derived or repeatable data such as:
- Bank indexes
- Search results
- Thumbnails
- Prompt previews
- Provider capability metadata
- Recently opened records

For every cache define:
- Source of truth
- Key and scope
- Lifetime
- Invalidation
- Size limit
- Offline behavior
- Rebuild behavior
- Protection against stale data overwriting newer durable state

## Memory and resource management
- Do not keep all full-resolution references and generated images decoded at once.
- Use thumbnails and release off-screen resources.
- Revoke or clean up temporary image and file handles when safe.
- Limit unbounded caches, undo histories, subscriptions, event listeners, background tasks, and retained previews.
- Cancel or ignore obsolete asynchronous work.
- Deduplicate requests and repeated processing.
- Monitor memory growth during long sessions and large histories.

## Failure behavior
Every operation should define:
- What remains on screen during failure
- What data is already durable
- Whether retry is safe
- Whether the user may continue editing
- How conflicts are shown
- How to return to the previous stable state

Generation, upload, analysis, search, persistence, or provider failures must not clear unrelated work.

## Perceived performance and polish
- Use meaningful skeletons, progress indicators, and preserved content instead of blank resets.
- Prefer optimistic interaction only when rollback is safe.
- Avoid layout shifts that move active controls.
- Keep the prompt editor usable while secondary content loads.
- Restore scroll, selection, and focus where it helps continuity.
- Do not use animation to hide slow behavior.

## Verification scenarios
Test at least:
- Long prompt typing during autosave
- Rapid lock and tag changes
- Navigation before save completes
- Refresh and restart
- Offline editing and reconnect
- Provider request failure and retry
- Reference upload or analysis interruption
- Large bank search
- Thousands of history or result items where the product permits it
- Repeated opening and closing of image viewers
- Backup, restore, and data migration
- Low-memory or resource-constrained conditions
- Two asynchronous responses arriving out of order

Completion requires evidence that these scenarios preserve user work and acceptable responsiveness.