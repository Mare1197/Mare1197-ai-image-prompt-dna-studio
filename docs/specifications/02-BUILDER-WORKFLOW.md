# Builder Workflow and Delivery Gates

This document defines how an AI builder should approach the project. It does not prescribe a technology stack or implementation structure.

## Gate 1 — Understand the product
- Read the specification index and the documents relevant to the current task.
- Inspect any existing implementation without assuming it is correct or required.
- Identify the main users, critical flows, product constraints, data that must persist, performance risks, integration boundaries, and acceptance criteria.
- Record assumptions instead of asking the user routine technical questions.

## Gate 2 — Create the plan
Produce a concise plan covering:
- Product scope and major user journeys
- System capabilities and dependencies
- Data ownership and persistence
- No-data-loss strategy
- Performance and caching strategy
- Accessibility and responsive behavior
- Security and safe rendering
- Testing and verification
- Delivery milestones and risk reduction

The plan may recommend architecture options, but it must not treat any previously suggested stack as mandatory.

## Gate 3 — Explore genuinely different designs
Before building the production UI, create at least four distinct UI/UX concepts.

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

Use any available design, UX, prototyping, visualization, image-generation, design-system, or accessibility skills and tools. Visual mockups or interactive prototypes are preferred over text-only descriptions.

For each direction provide:
- A name and design principle
- Main workspace visual
- Key screens or states
- Primary user flow
- Strengths and tradeoffs
- How clutter is prevented
- How it scales to advanced features
- Responsive behavior
- Accessibility considerations

At least one concept should favor beginner simplicity, one should favor a professional high-density workspace, and one should explore a distinctive interaction model while remaining practical.

## Gate 4 — User design approval
Present the concepts and recommend a direction, but do not choose on the user’s behalf.

Production UI implementation must wait for explicit approval of:
- One concept
- A hybrid of concepts
- Or a requested revision

This approval gate is mandatory. It is not an invitation to ask unrelated questions.

## Gate 5 — Choose the technical approach
After design approval, the builder chooses and documents the complete technical solution, including:
- Application architecture
- Frontend and backend approach
- Data storage and synchronization
- Local/offline behavior
- Image and reference storage
- Search and indexing
- Provider integration boundaries
- Testing approach
- Deployment and update strategy
- Performance and memory strategy

Choose based on the approved design and product requirements. Briefly justify the decisions. Do not select technology because it appeared in an older prompt.

## Gate 6 — Prove the critical workflow
Before scaling implementation across every feature, build one small end-to-end vertical slice using the approved design and selected architecture.

The slice should prove a realistic core journey such as:
- Enter and autosave a prompt draft
- Convert or edit Prompt DNA
- Add and persist a reference image
- Create a clean prompt
- Save a version or variation
- Restore the same work after reload or restart

The slice must include real data behavior, UI, persistence, recovery, error handling, and tests. Use it to validate the architecture and no-data-loss strategy early. Repair weaknesses before expanding the application.

This is an internal verification gate, not another routine user-approval checkpoint unless the prototype materially departs from the approved design.

## Gate 7 — Build in verifiable milestones
Break implementation into small end-to-end milestones. Each milestone should deliver a testable slice rather than disconnected layers.

A useful milestone should include the relevant:
- Data behavior
- Business rules
- UI and interaction
- Persistence and recovery
- Error handling
- Tests
- Documentation

Continue through routine milestones without requesting permission after every one.

## Gate 8 — Validate experience and resilience
Continuously verify:
- No prompt, reference, selection, lock, upload, workflow step, or history entry is lost unexpectedly
- Large banks and image histories remain responsive
- Loading and error states preserve context
- Keyboard and accessibility behavior works
- Responsive layouts remain usable
- Provider failures do not corrupt local work
- Cache invalidation never replaces durable data with stale state

## Gate 9 — Completion
The product is complete only when every criterion in `10-ACCEPTANCE-CRITERIA.md` has evidence.

Final delivery must include:
- Approved design record
- Technology and architecture decision record
- Feature checklist
- Test and verification evidence
- Data backup and recovery instructions
- Run, build, and deployment instructions
- Known limitations
- Remaining optional enhancements

## Context management
Read only the specifications and implementation areas needed for the active milestone. Large bank datasets, image histories, database migrations, and unrelated UI areas should not all be loaded together. Maintain concise project records so a future builder can continue without reconstructing the entire history.