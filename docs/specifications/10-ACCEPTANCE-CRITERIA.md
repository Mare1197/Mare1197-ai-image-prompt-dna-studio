# Acceptance Criteria

The product is complete only when the following are verified with evidence.

## Repository and branch safety
1. Design and implementation work occurred outside `main`.
2. `main` was not independently committed to, pushed to, rewritten, reset, rebased, force-pushed, repointed, or merged into by the builder.
3. The active design/build branch follows `<project-or-design-name>--<ai-model>--<harness>` or the separate implementation repository records an equivalent branch.
4. The full AI model and harness names are recorded.
5. The specification revision or control-point commit used by the build is recorded.

## Planning, reasoning, and architecture
6. The builder used high reasoning effort for architecture, UX, persistence, cache, concurrency, provider, and security decisions and recorded concise decision rationales.
7. The plan included active suggestions rather than only restating steps.
8. Suggestions were separated into Recommended, Optional, and Experimental with meaningful benefits and tradeoffs.
9. At least four genuinely different UI/UX concepts were created before production UI implementation.
10. The concepts differed in layout, information architecture, interaction flow, panel behavior, reference handling, and history/preview presentation—not only color.
11. The user explicitly approved a concept or hybrid, and the decision is recorded.
12. The builder selected and documented the complete technology and architecture approach after design approval.
13. A complete end-to-end vertical slice proved autosave, Prompt DNA, references, clean-prompt creation, version saving, and reload/restart recovery before broad implementation.
14. The final interface is modern, fabulous, cohesive, uncluttered, responsive, accessible, and suitable for beginners and advanced users.

## Design images and final visual evidence
15. `design images/README.md` exists and indexes every concept image, approved-design image, and final screenshot.
16. Each design concept has high-quality visuals in `design images/concepts/<concept-name>/`.
17. The approved or hybrid design is stored in `design images/approved-design/`.
18. Concept images are crisp, appropriately high resolution, properly composed, and free from avoidable stretching, visible compression, malformed subjects, or placeholder-like quality.
19. Original high-quality image sources are preserved separately from optimized delivery variants where appropriate.
20. Actual screenshots from the running implementation exist in `design images/final-screenshots/`.
21. Final screenshots include realistic populated views of the main workspace, main page, panels, pop-ups, menus, dialogs, drawers, overlays/layovers, image editing mode, references, Prompt DNA, characters, monsters, vehicles, banks, history, comparisons, settings, workspace variations, and important responsive and recovery states where applicable.
22. Final screenshots are clearly distinguished from concept mockups.

## Prompt DNA and prompting
23. Rough input converts to valid Prompt DNA and a coherent clean prompt.
24. DNA edits update the prompt live without losing cursor position or unrelated edits.
25. Every relevant field supports required lock, change, exclusion, and randomization states.
26. Five default variations are meaningfully distinct and preserve locks.
27. Only the active `CLEAN_RENDER_PROMPT` is submitted to providers.
28. Ordinary prompt entry never triggers generation automatically.
29. Positive reframing and conflict resolution work and explain adjustments.
30. Prompt scoring, linting, and repair work.

## History, references, and recovery
31. Prompt history supports branches, loading, diffs, restore, ratings, favorites, notes, and export.
32. Creating a branch never overwrites its parent or loses an unsaved draft.
33. Multiple references with roles and selective extraction work.
34. Reference images, roles, crops, focus regions, weights, notes, analysis, and relationships survive generation, navigation, reload, restart, and recoverable errors.
35. A failed upload, analysis, or generation does not clear the prompt, references, Prompt DNA, history, or previous results.
36. Prompt-box text remains until the user explicitly clears or replaces it.
37. Autosave, visible save status, undo/redo, checkpoints, session recovery, backup/restore, and import/export work.
38. Out-of-order asynchronous responses cannot overwrite newer edits.
39. Stored data migrates safely between supported data versions.

## Characters, monsters, wardrobe, and vehicles
40. Characters and monsters can be created, saved, loaded, and kept consistent.
41. Human and monster subjects remain distinct unless a transformation concept is explicitly requested.
42. Adult wardrobe contains approved lingerie, skirts, mini-skirts, heels, Vans, and similar slim sneakers.
43. Thick, platform, chunky, dad, wedge, heavy-lug, bulky, or oversized-foam footwear is blocked in banks, imports, presets, randomization, composition, linting, and result review.
44. The full approved vehicle library exists.
45. Cars support drift, heavy, track, street, widebody, show, luxury, and futuristic modifications.
46. Paint, wrap, livery, and decals are independent, editable, and lockable.
47. Exact vehicle locks preserve model, modifications, wheels, paint, wrap, livery, decals, and placement.

## Presets, results, workflows, and image editing
48. Presets apply partially without overwriting unrelated locks.
49. Result feedback creates a linked next iteration and stores reusable lessons with confidence.
50. Editable workflows, approval and audit history, undo/redo, and restore work.
51. Workflow progress survives navigation, reload, restart, and recoverable failure.
52. Image editing mode is accessible from the main workflow and preserves prompt, reference, history, and workspace state.

## Provider independence
53. ChatGPT Images and Nano Banana Pro adapters remain separate from universal Prompt DNA.
54. The app works in prompt-only mode without provider credentials.
55. Provider failures preserve local work and allow safe retry.

## Performance, image delivery, cache, and memory
56. The initial usable workspace does not require loading every bank, image, history item, or advanced editor.
57. Large banks, histories, and result collections use incremental loading, virtualization, pagination, or an equally effective approach.
58. Images use efficient thumbnails, responsive derivatives, or progressive loading and do not all remain decoded in memory.
59. High-quality original assets are not replaced by low-quality derivatives, and optimized delivery does not visibly degrade important UI imagery.
60. Cache sources, invalidation, size limits, and stale-data protection are documented and tested.
61. Caches are never the only copy of user work.
62. Obsolete asynchronous work, temporary image resources, listeners, and background tasks are cleaned up.
63. Prompt typing, DNA editing, search, panel interaction, and autosave remain responsive under realistic project sizes.
64. Long sessions and repeated viewer/editor use do not show unbounded memory growth.

## UI, accessibility, direct launch, and safety
65. The application opens directly into the usable main workspace.
66. No login, sign-up, account-creation, authentication-gate, welcome, marketing landing, onboarding-carousel, blocking splash, or mandatory setup-wizard page exists.
67. Any contextual first-run hints are dismissible, non-blocking, remembered after dismissal, and preserve all state.
68. Layout, filters, panels, themes, preview settings, active project, and active version persist appropriately.
69. Image history supports adjustable preview size, effective large-list browsing, enlarged viewing, keyboard navigation, and two/four-image comparison.
70. Desktop, tablet, and narrow-screen layouts remain usable without losing current work.
71. Keyboard navigation, focus visibility, screen-reader labeling, contrast, reduced motion, and accessible alternatives to drag-and-drop are verified.
72. All user-created text and imported data are handled safely; raw user HTML is never injected.
73. Destructive actions are explicit, understandable, and protected by confirmation or recovery where appropriate.

## Delivery and verification
74. Relevant automated and manual tests pass, or remaining failures are documented honestly.
75. Verification includes refresh, restart, offline/reconnect, provider failure, upload interruption, save failure, migration, backup/restore, large histories, constrained-memory scenarios, and visual screenshot review.
76. Documentation includes branch/repository identity, model/harness, build plan, suggestions, approved design, architecture decisions, data and recovery model, current state, testing evidence, known issues, run/build/deployment instructions, backup/restore instructions, and visual index.
77. Completion is not claimed until every applicable criterion above has evidence.