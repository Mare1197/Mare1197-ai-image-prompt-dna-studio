# UI, UX, and Workspace Requirements

## Mandatory design exploration
Before building the production interface, create at least four genuinely different UI/UX concepts and present them for user approval.

Use any available design, prototyping, visualization, image-generation, UX-research, design-system, motion, and accessibility skills or tools that improve the result. Use the highest reasoning effort available when evaluating layout, information architecture, complex interaction, clutter, responsiveness, and accessibility.

The concepts must not be palette swaps. Explore meaningful differences in:
- Information architecture
- Main navigation
- Workspace composition
- Panel, drawer, dock, overlay, and modal behavior
- Prompt-writing and Prompt DNA editing flow
- Bank discovery and selection
- Reference-image management
- Character, monster, and vehicle building
- Preview and history placement
- Beginner and expert modes
- Desktop, tablet, and narrow-screen adaptation

For each concept provide:
- High-quality visual mockups or prototypes
- Main workspace and key secondary views
- Design rationale
- Primary workflow
- Strengths and tradeoffs
- Clutter-prevention strategy
- Responsive behavior
- Accessibility considerations
- Recommended improvements and optional or experimental ideas

At least one direction should prioritize beginner simplicity, one a professional high-density workspace, and one a distinctive but practical interaction model.

Save concept images in `design images/concepts/<concept-name>/`. Save the approved or hybrid direction in `design images/approved-design/`.

The builder may recommend a direction, but production UI implementation must wait until the user explicitly approves one concept, a hybrid, or a revised direction.

## Direct-to-workspace launch
The application must open directly into the usable main workspace.

Do not create:
- Login or sign-up screens
- Account-creation menus
- Authentication gates
- Welcome pages
- Marketing landing pages
- Onboarding carousels
- Blocking splash screens
- Mandatory setup wizards

Optional contextual hints may exist only inside the workspace. They must be dismissible, non-blocking, remembered after dismissal, and unable to clear or replace user state.

## Design quality
The approved interface must feel fabulous, current, premium, and intentional while remaining calm and easy to understand.

Prioritize:
- Strong hierarchy
- Excellent spacing and typography
- Clear primary actions
- Progressive disclosure
- Contextual controls
- Consistent interaction patterns
- Fast perceived response
- Useful empty, loading, success, offline, conflict, error, and recovery states
- Reduced motion and accessible contrast
- Visual polish that supports work instead of adding decoration

Avoid:
- Dense walls of controls
- Permanent inspectors that consume space without context
- Excessive glow or animation
- Multiple overlapping floating windows
- Hidden destructive actions
- Color-only status communication
- Controls that reset unrelated state

## Image and visual asset quality
Use the highest-quality practical image assets in concepts and the finished interface.

- Prefer crisp, high-resolution, professionally composed, properly licensed, user-provided, or newly generated images.
- Avoid blurry, stretched, visibly compressed, malformed, low-detail, or placeholder-like assets when better images are available.
- Preserve original high-quality sources separately from optimized delivery variants.
- Use responsive derivatives, thumbnails, modern formats, progressive loading, and lazy loading.
- Never keep every full-resolution image decoded in memory.
- Do not sacrifice application responsiveness for raw resolution.
- High-quality imagery must support the workflow without adding clutter.

## Product capabilities the designs must accommodate
Provide intuitive access to:
- Prompt Architect
- Prompt DNA
- References
- Characters
- Monsters
- Vehicles
- Styles and effects
- Locations, camera, lighting, palette, mood, and materials
- Wardrobe and footwear
- Presets and recipes
- Prompt history and branching
- Generated results and comparison
- Workflows and approvals
- Settings, backups, recovery, and provider connections

These are capabilities, not a mandated navigation list. Organize them differently across design concepts where useful.

## Workspace behavior
The final workspace should support:
- A central creation and preview area
- A prominent but non-obstructive prompt editor
- Context-aware controls instead of every option appearing at once
- Resizable, collapsible, pinnable, or movable work areas where appropriate
- Focus modes for prompt editing, references, banks, Prompt DNA, history, image editing, and previews
- Saved layout preferences
- Clear active-version and save-state indicators
- Quick access to locks, requested changes, exclusions, and variation scope

Previous palettes may inspire the designs, but palette changes alone do not count as different concepts.

## Prompt editor
The prompt editor must:
- Support multi-line input and comfortable expansion
- Preserve all text until explicitly cleared or replaced
- Autosave and visibly show save state
- Survive navigation, generation, model changes, errors, reload, and restart
- Provide Rewrite, Improve, Build, Positive Reframe, Repair, Save, Copy, Variations, and explicit Generate actions
- Show the active clean prompt and distinguish drafts and notes
- Show relevant references, locks, and output settings without overcrowding

## Reference experience
- Persist uploaded references immediately and keep them after generation, navigation, reload, and restart.
- Persist roles, crops, weights, focus regions, notes, analysis, and locks.
- Upload or analysis failure must not clear a reference.
- Replacement or deletion must be explicit.
- Show which prompt version and DNA fields use each reference.

## Image editing mode
Provide a focused image-editing workspace or mode that supports the implemented image-editing capabilities without losing prompt, reference, history, or workspace state. It must be accessible from the main workflow and must not require a separate login, welcome page, or disconnected application shell.

## Compact output controls
Use clear compact controls for aspect ratio and similar output choices. Default ratio is 16:9. Common ratios include 1:1, 4:5, 3:4, 2:3, 3:2, 16:9, 9:16, and 21:9.

Do not add sampler, scheduler, guidance, prompt-strength, or reference-strength controls.

## Tag and constraint interaction
Support:
- Select
- Exact or approximate lock
- Exclude
- Request change
- Randomize
- Multi-select
- Category-level actions
- Preserve/change/randomize checklists

The final pattern may use clicks, modifier keys, context menus, touch alternatives, or another approved interaction. Status must not rely on color alone.

## Image history and comparison
Support:
- Batch rows or an equally effective history view
- Adjustable preview size
- Adaptive density
- Enlarged viewer
- Thumbnail navigation
- Keyboard navigation and looping
- Escape to close
- Two-image and four-image comparison
- Prompt and DNA differences
- Favorite, rating, notes, save as reference, save as preset, and create variation

## Responsive behavior
The product remains usable across desktop, tablet, and narrower screens. Advanced density may adapt instead of forcing the desktop layout onto small viewports. Preserve prompt drafts, references, and the current task during layout transitions.

## Accessibility
Provide full keyboard navigation, visible focus, screen-reader labels, logical reading order, sufficient contrast, reduced motion, accessible drag-and-drop alternatives, clear recovery actions, and device-appropriate touch targets.

## Persistence of workspace state
Remember panels, overlays, menus, filters, searches, selections, theme, preview size, comparison state, open project, active version, useful scroll positions, and current workflow step. Temporary presentation state may reset only when it cannot erase or confuse user work.

## Required final screenshots
Before completion, capture actual screenshots from the running implementation and save them in `design images/final-screenshots/`.

Include realistic populated views of:
- Main page and Prompt Architect workspace
- Contextual and pinned panels
- Pop-ups, menus, dialogs, drawers, overlays, and layovers
- Image editing mode
- References and Prompt DNA editing
- Character, monster, and vehicle workspaces
- Relevant bank browsers
- History, branching, comparisons, and enlarged viewer
- Different workspace layouts or modes
- Settings, provider connections, backup, recovery, and accessibility controls
- Narrow-screen or tablet adaptation
- Loading, empty, save, offline, conflict, error, retry, and recovery states

These must be screenshots of the real application rather than concept mockups. Index and describe them in `design images/README.md`.