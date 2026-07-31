# UI, UX, and Workspace Requirements

## Mandatory design exploration
Before building the production interface, the builder must create at least four genuinely different UI/UX concepts and present them for user approval.

Use any available design, prototyping, visualization, image-generation, UX-research, design-system, motion, and accessibility skills or tools that can improve the outcome.

The concepts must not be palette swaps. They should explore meaningful differences in:
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
- A visual mockup or prototype when tools permit
- Main workspace and key secondary views
- A short design rationale
- Primary workflow
- Strengths and tradeoffs
- Clutter-prevention strategy
- Responsive behavior
- Accessibility considerations

At least one direction should prioritize beginner simplicity, one should prioritize a professional high-density workspace, and one should explore a distinctive but practical interaction model.

The builder may recommend a direction, but production UI implementation must wait until the user explicitly approves one concept, a hybrid, or a revised direction.

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
- Useful empty, loading, success, offline, conflict, and error states
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

## Product capabilities the designs must accommodate
The approved design must provide intuitive access to:
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

These are capabilities, not a mandated navigation list. The builder may organize them differently in each design concept.

## Workspace behavior
The final workspace should support:
- A central creation and preview area
- A prominent but non-obstructive prompt editor
- Context-aware controls rather than every option being visible at once
- Resizable, collapsible, pinnable, or movable work areas where appropriate
- A way to expand or focus on prompt editing, references, banks, Prompt DNA, history, and previews
- Saved layout preferences
- Clear active-version and save-state indicators
- Quick access to locks, requested changes, exclusions, and variation scope

Previous visual directions such as graphite/black, midnight purple, purple-cyan-pink, graphite-teal-electric-blue-acid-lime, black/bright-green, high-contrast dark, and clean light may be used as inspiration, but they must not be treated as the design concepts themselves.

## Prompt editor requirements
The prompt editor must:
- Support multi-line input and comfortable expansion
- Preserve all text until the user explicitly clears or replaces it
- Autosave and visibly show save state
- Survive navigation, generation, model changes, errors, reload, and restart
- Provide Rewrite, Improve, Build, Positive Reframe, Repair, Save, Copy, Variations, and explicit Generate actions
- Show the active clean prompt and distinguish it from drafts and notes
- Show relevant references, locks, and output settings without overcrowding the editor

## Reference experience
- Uploaded reference images must persist immediately and remain after generation, navigation, reload, and restart.
- Reference roles, crops, weights, focus regions, notes, analysis, and locks must persist.
- Upload or analysis failure must not clear the reference.
- Replacing or deleting a reference must be explicit.
- The user must be able to see which prompt version and DNA fields use each reference.

## Compact output controls
Use clear compact controls for aspect ratio and other simple output choices. Default aspect ratio is 16:9 and common ratios include 1:1, 4:5, 3:4, 2:3, 3:2, 16:9, 9:16, and 21:9.

Do not add sampler, scheduler, guidance, prompt-strength, or reference-strength controls.

## Tag and constraint interaction
Support efficient interaction for:
- Select
- Lock exactly or approximately
- Exclude
- Request change
- Randomize
- Multi-select
- Category-level actions
- Preserve/change/randomize checklists

The final interactions may use clicks, modifier keys, context menus, touch alternatives, or another approved pattern. Status must not rely on color alone.

## Image history and comparison
Support:
- Batch rows or an equally effective history presentation
- Adjustable preview size
- Adaptive item density
- Enlarged viewer
- Thumbnail navigation
- Keyboard navigation and looping
- Escape to close
- Two-image and four-image comparison
- Prompt and DNA differences
- Favorite, rating, notes, save as reference, save as preset, and create variation

## Responsive behavior
The product should remain usable across desktop, tablet, and narrower screens. Advanced density may adapt rather than forcing the desktop layout into a small viewport. Preserve the prompt draft, references, and current task during layout transitions.

## Accessibility
Provide:
- Full keyboard navigation
- Visible focus
- Screen-reader labels
- Logical reading and tab order
- Sufficient contrast
- Reduced-motion mode
- Accessible drag-and-drop alternatives
- Clear errors and recovery actions
- Touch targets suitable for the current device

## Persistence of workspace state
Remember panels, overlays, menus, filters, search queries, selections, theme, preview size, comparison state, open project, active version, scroll position where useful, and current workflow step. Temporary presentation state may reset only when doing so cannot erase or confuse user work.