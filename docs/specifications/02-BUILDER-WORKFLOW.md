# Builder Workflow and Delivery Gates

This document defines how an AI builder approaches the project. It does not prescribe a technology stack or implementation structure.

## Gate 0 — Protect the control branch
Before any design or implementation write:
- Inspect the repository, remotes, current branch, and working tree.
- Treat `main` as a read-only specification and control point.
- Never commit, push, merge, reset, rewrite, rebase, squash, force-push, delete, or repoint `main` independently.
- If currently on `main`, create and switch to a branch named `<project-or-design-name>--<ai-model>--<harness>`.
- Record the full model and harness names.
- A separate implementation repository must also preserve its default branch as a clean control point and use a named branch for generated work.

Follow `12-BRANCH-SAFETY-AND-VISUAL-EVIDENCE.md`.

## Gate 1 — Understand the product deeply
- Read the specification index and the documents relevant to the current task.
- Inspect existing implementation without assuming it is correct or required.
- Use the highest reasoning effort available.
- Identify users, critical flows, constraints, durable data, performance risks, integration boundaries, failure modes, and acceptance criteria.
- Compare plausible approaches and challenge weak assumptions.
- Record assumptions instead of asking routine technical questions.

## Gate 2 — Create a plan with active suggestions
Produce a concise plan covering:
- Product scope and major user journeys
- System capabilities and dependencies
- Data ownership and persistence
- No-data-loss strategy
- Performance, cache, loading, and memory strategy
- Accessibility and responsive behavior
- Security and safe rendering
- Testing and verification
- Delivery milestones and risk reduction

Do not merely convert the specification into a checklist. Provide active suggestions grouped as:

### Recommended
Improvements that materially strengthen quality, usability, resilience, maintainability, or safety.

### Optional
Useful additions that can follow the first complete version.

### Experimental
Distinctive or higher-risk ideas requiring approval before they materially alter the product.

For meaningful suggestions, explain benefit, cost, risk, and tradeoff. Never silently remove a hard requirement.

## Gate 3 — Explore genuinely different designs
Before production UI implementation, create at least four distinct UI/UX concepts.

The concepts must differ in more than color or typography. Explore meaningful alternatives in:
- Navigation model
- Information architecture
- Workspace composition
- Panel and overlay behavior
- Prompt authoring flow
- Prompt DNA visibility
- Bank browsing and tag selection
- Character, monster, and vehicle editing
- Reference-image management
- Preview and history presentation
- Beginner versus expert density
- Desktop, tablet, and narrow-screen adaptation

Use any available design, UX, prototyping, visualization, image-generation, design-system, or accessibility skills and tools.

Use the highest-quality practical images available. Concept visuals must be crisp, high resolution, properly composed, and free from obvious distortion, compression artifacts, or placeholder-like quality.

Save each direction in:

`design images/concepts/<concept-name>/`

For each direction provide:
- A name and design principle
- Main workspace visual
- Key screens or states
- Primary user flow
- Strengths and tradeoffs
- Clutter-prevention strategy
- Responsive behavior
- Accessibility considerations

At least one concept should favor beginner simplicity, one a professional high-density workspace, and one a distinctive but practical interaction model.

## Gate 4 — User design approval
Present the concepts and recommend a direction, but do not choose on the user’s behalf.

Production UI implementation waits for explicit approval of:
- One concept
- A hybrid
- Or a requested revision

Save the approved direction and any hybrid revisions in:

`design images/approved-design/`

This approval gate is mandatory but is not an invitation to ask unrelated questions.

## Gate 5 — Choose the technical approach
After design approval, choose and document the complete technical solution:
- Application architecture
- Frontend and backend approach
- Data storage and synchronization
- Local and offline behavior
- Image and reference storage
- Search and indexing
- Provider boundaries
- Testing
- Deployment and updates
- Performance, cache, and memory strategy

Choose based on the approved design and product requirements. Briefly justify decisions and alternatives. Do not select technology because it appeared in an older prompt.

## Gate 6 — Prove the critical workflow
Before broad implementation, build one end-to-end vertical slice:
- Enter and autosave a prompt
- Convert or edit Prompt DNA
- Add and persist a reference image
- Create a clean prompt
- Save a version or variation
- Restore the same work after reload or restart

Include real UI, persistence, recovery, errors, and tests. Repair weaknesses before scaling.

This is an internal verification gate, not another routine approval checkpoint unless it materially departs from the approved design.

## Gate 7 — Build in verifiable milestones
Deliver small end-to-end milestones rather than disconnected layers.

Each milestone includes the relevant:
- Data behavior
- Business rules
- UI and interaction
- Persistence and recovery
- Error handling
- Tests
- Documentation

Continue through routine milestones without requesting permission after each one.

## Gate 8 — Validate experience and resilience
Continuously verify:
- No prompt, reference, selection, lock, upload, workflow step, or history entry is lost
- Large banks and image histories remain responsive
- Loading and error states preserve context
- Keyboard and accessibility behavior works
- Responsive layouts remain usable
- Provider failures do not corrupt local work
- Cache invalidation cannot replace newer durable data with stale state
- Long sessions do not accumulate unbounded memory
- High-resolution images use optimized derivatives and do not all remain decoded at once

## Gate 9 — Capture final visual evidence
Before completion is claimed:
- Run the real application with realistic populated data.
- Capture high-resolution screenshots of the main workspace, panels, pop-ups, dialogs, drawers, overlays, image editing mode, references, DNA editing, bank browsers, workspaces, settings, comparisons, responsive states, and recovery/error states.
- Save them in `design images/final-screenshots/`.
- Maintain `design images/README.md` with an image index and clear concept-versus-real-screenshot labels.

Do not substitute concept mockups for actual screenshots of the build.

## Gate 10 — Completion
The product is complete only when every criterion in `10-ACCEPTANCE-CRITERIA.md` has evidence.

Final delivery includes:
- Branch/repository, model, and harness record
- Planning suggestions and decisions
- Approved design record
- Technology and architecture decisions
- Feature checklist
- Test and verification evidence
- Data backup and recovery instructions
- Run, build, and deployment instructions
- Design-image and final-screenshot index
- Known limitations
- Remaining optional enhancements

## No login or welcome flow
The implementation must open directly into the usable main workspace. Do not add login, sign-up, authentication gates, welcome pages, marketing landing pages, onboarding carousels, blocking splash pages, or mandatory setup wizards.

## Context management
Read only the specifications and implementation areas needed for the active milestone. Do not load every bank, history, migration, image, and UI area together. Maintain concise records so a future builder can continue without reconstructing history.