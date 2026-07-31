# Branch Safety, Builder Identity, Design Images, and Final Visual Evidence

## Intended repository name
The specification repository is intended to be named:

`Mare1197/Mare1197-ai-image-prompt-dna-studio-instructions`

This repository is a control point and specification source. It is not the place for an AI builder to write experimental design or implementation work directly onto `main`.

## `main` is a protected control point
Treat `main` as read-only unless the user explicitly instructs an exact specification change on `main`.

An AI builder must never independently:
- Commit design or implementation work directly to `main`
- Push generated code or visual experiments to `main`
- Rewrite, reset, rebase, squash, force-push, delete, replace, or repoint `main`
- Merge a build branch into `main`
- Interpret broad commands such as “build it,” “continue,” “fix it,” or “finish it” as permission to modify `main`

Before any design or implementation write:
1. Inspect the current repository, branch, remote, and working tree.
2. Confirm that the active branch is not `main`.
3. Create and switch to a new correctly named branch, or create a separate implementation repository when explicitly requested or when that is safer.
4. Record the branch or repository identity before continuing.

The builder may fetch, compare against, or restore context from `main` at any time. `main` remains the stable control and comparison point.

## Required branch naming
Every AI-created design or implementation branch must identify:
- The project or design direction
- The AI model used
- The harness, coding environment, or builder used

Format:

`<project-or-design-name>--<ai-model>--<harness>`

Examples:
- `prompt-dna-studio--gpt-5-6--codex`
- `professional-workspace--claude-sonnet--claude-code`
- `approved-hybrid-ui--gemini-pro--antigravity`

Use lowercase, filesystem-safe slugs. Add a short sequence or date only when a collision must be avoided.

The branch description, project records, or README must also record the full human-readable model and harness names.

## Separate implementation repositories
When the user instructs the builder to create a separate implementation repository:
- Preserve its default branch as a clean control/reference point.
- Create the named design/build branch before implementation.
- Do not silently place generated implementation on the default branch.
- Keep a clear link back to this specification repository and the exact specification revision used.

## Planning must include active suggestions
The builder must use high reasoning effort and critically improve the plan rather than merely restating requested steps.

During planning, provide:
- Recommended improvements
- Optional enhancements
- Experimental ideas
- Missing workflows or product gaps
- UX risks and clutter risks
- Performance, persistence, cache, memory, and failure risks
- Architecture alternatives and tradeoffs
- Simplification opportunities that preserve capability
- Testing and verification suggestions

Separate suggestions into:
- **Recommended:** should be included because they materially improve quality or safety
- **Optional:** useful but not required for the first complete version
- **Experimental:** higher-risk or distinctive ideas that require approval

Explain the likely benefit, cost, and tradeoff of each meaningful suggestion. Never silently remove or weaken hard requirements.

## Highest reasoning standard
For architecture, data durability, state management, complex UX, concurrency, provider integration, and security decisions:
- Use the highest reasoning effort available in the active model or harness.
- Inspect evidence and existing behavior before deciding.
- Compare plausible alternatives.
- Challenge assumptions and identify edge cases.
- Prefer verified, maintainable decisions over quick guesses.
- Record decisions and reasons without exposing private chain-of-thought.
- Run tests and visual verification before claiming success.

## Required `design images` folder
Every design or implementation branch, and every separate implementation repository, must contain:

`design images/`

Use this structure:

```text
 design images/
 ├── README.md
 ├── concepts/
 │   ├── <concept-name>/
 │   └── ...
 ├── approved-design/
 └── final-screenshots/
```

The folder’s `README.md` must provide an index with:
- File name
- Concept or application state
- Date or build revision
- Viewport or device class
- Whether the image is a concept, prototype, or actual application screenshot

## Design concept images
Before production UI implementation:
- Create at least four structurally different concepts.
- Save visual outputs in `design images/concepts/<concept-name>/`.
- Include the main workspace and enough key views to understand the concept.
- Use the highest-quality images practical for the available tools.
- Do not submit compressed, blurry, stretched, placeholder-like, or low-detail design images when higher-quality output is available.
- Concepts must differ in layout and interaction, not only palette.

After user approval:
- Save the chosen concept, hybrid, and revisions in `design images/approved-design/`.
- Record which source concepts were combined and what changed.

## Image quality rules for UI generation
When generating or selecting imagery for concept designs or the implemented UI:
- Use the highest-quality and highest-resolution practical source images.
- Prefer crisp, professional, properly composed images suited to the displayed size.
- Preserve original high-quality sources separately from optimized delivery derivatives.
- Never upscale tiny images and present them as high quality.
- Avoid visible compression artifacts, poor masking, distorted vehicles, malformed subjects, unreadable details, or obvious placeholder imagery.
- Use legally usable, properly licensed, user-provided, or newly generated assets.
- Use responsive derivatives, thumbnails, modern formats, progressive loading, and lazy loading so visual quality does not make the application slow.
- Do not decode or retain every full-resolution image in memory at once.
- Use high-quality images to improve the interface, not to create clutter or distract from the workflow.

## Final screenshots of the running application
Before completion is claimed, capture actual screenshots from the implemented and running application. Save them in:

`design images/final-screenshots/`

These must not be concept mockups. They must demonstrate the real build with realistic populated data.

Capture, where applicable:
- Main Prompt Architect workspace
- Main page with a realistic prompt, DNA, references, and results
- Contextual, resizable, and pinned panels
- Pop-ups, context menus, dropdowns, dialogs, drawers, overlays, and layovers
- Image editing mode and editing controls
- Reference-image workflow
- Prompt DNA editing mode
- Character workspace
- Monster/creature workspace
- Vehicle workspace
- Style and effect banks
- Wardrobe and footwear bank
- Wrap, racing-livery, and decal controls
- Prompt history and branching
- Two-image and four-image comparisons
- Enlarged image viewer
- Different workspace layouts or modes
- Settings
- Provider connections
- Backup, restore, recovery, and import/export
- Accessibility and reduced-motion controls
- Tablet or narrow-screen adaptation
- Important loading, empty, save, offline, conflict, error, retry, and recovery states

Screenshots should be clear, high resolution, consistently framed, and labeled in the visual index.

## No login, welcome, or marketing pages
Do not create:
- Login screens
- Sign-up screens
- Account creation menus
- Authentication gates
- Welcome pages
- Marketing landing pages
- Splash pages that block the workspace
- Onboarding carousels
- Mandatory setup wizards

The application must open directly into the usable main workspace.

Optional contextual hints may appear inside the workspace only when they are:
- Dismissible
- Non-blocking
- Remembered after dismissal
- Never destructive to existing state

## Completion rule
Completion cannot be claimed unless:
- Work happened outside `main` on a correctly named branch or separate repository.
- The model and harness used are recorded.
- Concept images are present in `design images/concepts/`.
- The approved design is present in `design images/approved-design/`.
- Actual final screenshots are present in `design images/final-screenshots/`.
- The visual index distinguishes concepts from real application screenshots.
- No login, welcome, or marketing surface blocks access to the workspace.
