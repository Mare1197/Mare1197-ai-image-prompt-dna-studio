# Acceptance Criteria

The product is complete only when the following are verified with evidence.

## Design and architecture
1. At least four genuinely different UI/UX concepts were created before production UI implementation.
2. The concepts differed in layout, information architecture, interaction flow, panel behavior, reference handling, and history/preview presentation—not only color.
3. The user explicitly approved a concept or hybrid, and the decision is recorded.
4. The builder selected and documented the complete technology and architecture approach after design approval.
5. The final interface is modern, fabulous, cohesive, uncluttered, responsive, accessible, and appropriate for both beginners and advanced users.

## Prompt DNA and prompting
6. Rough input converts to valid Prompt DNA and a coherent clean prompt.
7. DNA edits update the prompt live without losing cursor position or unrelated edits.
8. Every relevant field supports required lock, change, exclusion, and randomization states.
9. Five default variations are meaningfully distinct and preserve locks.
10. Only the active `CLEAN_RENDER_PROMPT` is submitted to providers.
11. Ordinary prompt entry never triggers generation automatically.
12. Positive reframing and conflict resolution work and explain adjustments.
13. Prompt scoring, linting, and repair work.

## History, references, and recovery
14. Prompt history supports branches, loading, diffs, restore, ratings, favorites, notes, and export.
15. Creating a branch never overwrites its parent or loses an unsaved draft.
16. Multiple references with roles and selective extraction work.
17. Reference images, roles, crops, focus regions, weights, notes, analysis, and relationships survive generation, navigation, reload, restart, and recoverable errors.
18. A failed upload, analysis, or generation does not clear the prompt, references, Prompt DNA, history, or previous results.
19. Prompt-box text remains until the user explicitly clears or replaces it.
20. Autosave, visible save status, undo/redo, checkpoints, session recovery, backup/restore, and import/export work.
21. Out-of-order asynchronous responses cannot overwrite newer edits.
22. Stored data can migrate safely between supported data versions.

## Characters, monsters, wardrobe, and vehicles
23. Characters and monsters can be created, saved, loaded, and kept consistent.
24. Human and monster subjects remain distinct unless a transformation concept is explicitly requested.
25. Adult wardrobe contains approved lingerie, skirts, mini-skirts, heels, Vans, and similar slim sneakers.
26. Thick, platform, chunky, dad, wedge, heavy-lug, bulky, or oversized-foam footwear is blocked in banks, imports, presets, randomization, composition, linting, and result review.
27. The full approved vehicle library exists.
28. Cars support drift, heavy, track, street, widebody, show, luxury, and futuristic modifications.
29. Paint, wrap, livery, and decals are independent, editable, and lockable.
30. Exact vehicle locks preserve model, modifications, wheels, paint, wrap, livery, decals, and placement.

## Presets, results, and workflows
31. Presets can apply partially without overwriting unrelated locks.
32. Result feedback creates a linked next iteration and stores reusable lessons with confidence.
33. Editable workflows, approval and audit history, undo/redo, and restore work.
34. Workflow progress survives navigation, reload, restart, and recoverable failure.

## Provider independence
35. ChatGPT Images and Nano Banana Pro adapters remain separate from universal Prompt DNA.
36. The app works in prompt-only mode without provider credentials.
37. Provider failures preserve local work and allow safe retry.

## Performance, cache, and memory
38. The initial usable workspace does not require loading every bank, image, history item, or advanced editor.
39. Large banks, histories, and result collections use incremental loading, virtualization, pagination, or an equally effective approach.
40. Images use efficient thumbnails or progressive loading and do not all remain decoded in memory.
41. Cache sources, invalidation, size limits, and stale-data protection are documented and tested.
42. Caches are never the only copy of user work.
43. Obsolete asynchronous work, temporary image resources, listeners, and background tasks are cleaned up.
44. Prompt typing, DNA editing, search, panel interaction, and autosave remain responsive under realistic project sizes.
45. Long sessions and repeated viewer use do not show unbounded memory growth.

## UI, accessibility, and safety
46. Layout, filters, panels, themes, preview settings, active project, and active version persist appropriately.
47. Image history supports adjustable preview size, effective large-list browsing, enlarged viewing, keyboard navigation, and two/four-image comparison.
48. Desktop, tablet, and narrow-screen layouts remain usable without losing current work.
49. Keyboard navigation, focus visibility, screen-reader labeling, contrast, reduced motion, and accessible alternatives to drag-and-drop are verified.
50. All user-created text and imported data are handled safely; raw user HTML is never injected.
51. Destructive actions are explicit, understandable, and protected by confirmation or recovery where appropriate.

## Delivery and verification
52. Relevant automated and manual tests pass, or remaining failures are documented honestly.
53. Verification includes refresh, restart, offline/reconnect, provider failure, upload interruption, save failure, migration, backup/restore, large histories, and constrained-memory scenarios.
54. Documentation includes the build plan, approved design, architecture decisions, data and recovery model, current state, testing evidence, known issues, run/build/deployment instructions, and backup/restore instructions.
55. Completion is not claimed until every applicable criterion above has evidence.