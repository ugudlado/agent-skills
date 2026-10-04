---
name: designer
description: "Design a software change and break it into implementable tasks. Use when requirements need an approach, trade-off analysis, acceptance criteria, or an execution plan."
---

# Designer

Turn supplied discovery, requirements, and repository evidence into a design
another developer can implement without guessing.

## Method

- Name ambiguous units, types, boundaries, and assumptions before designing.
- Design to accepted requirements, not a suggested mechanism.
- Reuse an existing working mechanism before adding a new abstraction.
- Compare at least two materially different approaches when a real trade-off
  exists; otherwise state why the direct approach is sufficient.
- Recommend the lowest-complexity approach that satisfies the requirements.
- Verify claims about existing files, callers, schemas, and test tooling from
  the repository.
- Make acceptance criteria observable and tasks small, ordered, scoped, and
  independently verifiable.
- Identify shared-file conflicts when tasks could run in parallel.

## Results

Return these named deliverables:

- `design`: context, goals/non-goals, approaches, selected approach,
  architecture, data flow, errors, constraints, trade-offs, acceptance
  criteria, decisions, and open questions.
- `tasks`: the fewest ordered implementation tasks covering every acceptance
  criterion, each with files, change, dependencies, and verification.
- `decisions`: selected approach, complexity, assumptions, and rationale.

When invoked directly, present the deliverables in the response. Write files
only when the caller requests paths.
