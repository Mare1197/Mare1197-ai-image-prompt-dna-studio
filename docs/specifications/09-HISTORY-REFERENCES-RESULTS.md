# History, References, Results, and Learning

## Prompt history
Original input is `0P`. Major rewrites use `V1`, `V2`, and so on. Branches use the parent plus a short direction and sequence, such as `V1-Cinematic-1` or `V2-Wrap-1`.

Each record stores its identity, title, parent, Prompt DNA, clean prompt, adapter output, references, locks, changes, rating, favorite state, notes, timestamps, and recovery metadata.

Support:
- Tree, timeline, and compact-list views
- Search and filters
- Prompt and DNA diffs
- Restore and duplicate
- Favorite and rating
- Notes
- Export
- Active-version selection
- Recovery from an interrupted edit

History writes must be durable. Creating a new branch must never overwrite its parent or silently discard an unsaved draft.

## References
Support at least four active references, with an architecture that can grow when appropriate.

Reference roles include:
- Whole composition
- Identity, face, or body
- Wardrobe, lingerie, footwear, or pose
- Monster design or surface
- Vehicle model, shape, body kit, wheels, paint, wrap, livery, or decals
- Camera, lighting, palette, environment, texture, mood, or style

Each reference stores:
- Durable identity and project relationship
- Role
- Weight and priority
- Lock status
- Include or ignore status
- Crop and focus region
- Notes and analysis
- Prompt versions and DNA fields that use it
- Upload and processing status

## Reference durability rules
- Persist the original reference or a durable retrievable representation immediately after selection.
- Preserve references through generation, navigation, model changes, validation errors, provider failures, reload, restart, and application updates.
- Never clear a reference because an unrelated action completed or failed.
- Preserve crop, role, weight, focus, analysis, and lock state.
- Failed upload or analysis must retain the local selection and provide retry or replacement options.
- Deletion and replacement must be explicit and should be undoable when practical.
- Selective extraction may populate only chosen DNA fields and must not overwrite unrelated locks.

## Result feedback
Evaluate:
- Character count, identity, wardrobe, lingerie, footwear, and sole thickness
- Monster type, scale, anatomy, and human-monster separation
- Vehicle model, modifications, wheels, stance, paint, wrap, livery, and decals
- Composition, camera, lighting, style, effects, and environment
- Technical quality and creative success

The feedback loop must:
1. Record successful and failed details.
2. Suggest the smallest useful correction.
3. Offer to lock successful fields.
4. Create a linked next branch.
5. Preserve the reviewed result and source version.
6. Separate global, project, preset, and provider-specific lessons.
7. Use confidence labels and avoid treating one accident as a universal rule.

## Generation and review failure behavior
A failed generation, cancelled request, disconnected provider, invalid response, or review error must not alter the active draft, Prompt DNA, references, history, or previous results. Preserve the attempted request and enough status information to retry safely.

## Copy and export
Copy the clean prompt, provider-adapted prompt, Prompt DNA, positive reframing, tags, locks, variations, full prompt pack, history, preset, and result notes.

Export plain text, Markdown, structured data, Prompt DNA, project packages, history, presets, references metadata, and result reviews. Backup and restore must preserve relationships among prompts, references, versions, results, and lessons.