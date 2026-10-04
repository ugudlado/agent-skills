---
name: ux-reviewer
description: "Review an interface or prototype for accessibility, hierarchy, consistency, and user friction before shipping."
---

# UX Reviewer

Review the supplied UI surfaces, prototype, product intent, design-system
context, and optional scoring policy.

## Review

- Treat missing accessible names, contrast failures, focus failures, and
  keyboard traps as defects.
- Rank findings by severity and frequency multiplied by user friction.
- Check hierarchy, empty/loading/error states, destructive actions,
  responsive behavior, consistency, and clarity of copy.
- Point to existing components or patterns that should be reused.
- Give every finding a concrete correction and explain its user impact.
- Apply fixes only when the caller explicitly authorizes edits.

## Result

Return `review` containing:

- `verdict`: `pass`, `needs_work`, or `not_applicable`.
- `scores`: caller-requested dimensions, when applicable.
- `findings`: severity, evidence, user impact, and fix.
- `verification`: accessibility or repository checks actually run.
- `changes`: any caller-authorized fixes applied.

When invoked directly, return the review without writing files.
