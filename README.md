# agent-skills

Reusable agent skills (SKILL.md format), promoted one-way from a private repo. Issues welcome.

| Skill | Description |
|---|---|
| `code-reviewer` | Review a code change or PR from every angle in one pass: requirement compliance, correctness, security, over-engineering (what to delete), and reuse/efficiency. Use for implementation review, PR review, merge readiness, 'what can we delete', or 'simplify review'. |
| `design-reviewer` | Review a software design and task plan for completeness, feasibility, traceability, and scope control before implementation. |
| `designer` | Design a software change and break it into implementable tasks. Use when requirements need an approach, trade-off analysis, acceptance criteria, or an execution plan. |
| `developer` | Implement a software change from a work brief or task plan. Use for scoped code changes that require repository investigation, tests, and verification. |
| `explorer` | Investigate a codebase, discover change scope, or diagnose a bug with evidence. Use for read-only surveys, impact analysis, and root-cause work. |
| `humanizer` | Rewrite text to sound natural and specific while preserving meaning. Use when the user asks to humanize prose or remove AI writing patterns. |
| `ideator` | Generate, refresh, and prioritize product or engineering ideas using current evidence. Use for brainstorming, backlog triage, or choosing what to build next. |
| `learner` | Reflect on completed work and turn observed failures or successes into durable, testable process improvements. Use for retrospectives and prompt or workflow learning. |
| `qa-tester` | Verify acceptance criteria on a running build with browser evidence and record pass/fail per item. Use for QA passes, acceptance checks on a preview or a locally served branch, and before/after screenshots. |
| `ux-designer` | Design user flows, interface direction, and prototypes for a real product constraint. Use for UX exploration, interaction design, or interface prototyping. |
| `ux-evaluator` | Score a rendered UI with a hard-fail UX floor then four weighted taste axes. Use in loop-design, or when the user wants a graded product-UI critique with Chrome verification. Not a one-shot shipping review (use ux-reviewer) and not a software-design review (use design-reviewer). |
| `ux-generator` | Edit a target UI file in a design loop. Use when loop-design is running, when iterating a prototype HTML, or when the user wants a generator pass on a product UI. Not for one-shot UX exploration (use ux-designer) or shipping review (use ux-reviewer). |
| `ux-reviewer` | Review an interface or prototype for accessibility, hierarchy, consistency, and user friction before shipping. |

## License

MIT, see [LICENSE](LICENSE).
