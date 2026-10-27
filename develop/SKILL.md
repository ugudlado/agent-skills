---
name: develop
description: "Take a software change from request or ticket to a reviewed pull request: criteria, understand, plan, plan review, implement, review, ship, learn. Use for any feature, bug fix, or refactor that should end in a PR with evidence per criterion."
---

# Develop

Run one software change end to end. Each stage names an existing role skill;
load it and follow it. This skill does not restate their rules. It says when
to use each, what each hands to the next, and where to stop.

## Stages

1. **Criteria.** List the acceptance criteria, explicit or implied by the
   title and description. If one is unclear with no sensible default: ask one
   question when a human is present, otherwise record the assumption and go on.
2. **Understand.** `explorer`: `discovery` for a feature, `diagnosis` for a
   bug (red loop first). Hands on: scope, constraints, or root cause.
3. **Plan.** A UI change runs `ux-designer` for the flow first, then
   `designer`; both research with web search when available. `designer`:
   ordered tasks, each with files and its own verification. Bug: the
   diagnosis plus the minimal fix is the plan; skip discovery and `designer`.
4. **Plan review.** `design-reviewer`, fresh context, strongest available
   model. At most 2 rounds; fix findings between rounds.
5. **Implement.** `developer`, task by task in plan order. Independent tasks
   may go to subagents on a cheaper model; each brief carries the task, the
   files, the constraints and the verification commands, and the subagent
   loads `developer` itself. Read every diff yourself: a report is a claim.
6. **Review.** `code-reviewer`, fresh context, strongest available model.
   At most 3 rounds; findings still open after round 3 go under "Open issues".
   A visible change (a screen, page, rendered email or chart, CLI output a
   person reads) needs screenshots of every changed screen: after, plus before
   when an existing screen changed. Seeded or test data only, never secrets or
   real user data. Use `qa-tester` (or `browser-testing`) where a browser is
   available. The reviewer gets them; none on a visible change is a required
   fix unless the reason they could not be captured is recorded.
7. **Ship.** Re-run final verification, then commit, push and open a PR whose
   body maps each criterion to its evidence. Never merge. Screenshots go in
   the PR body itself: pass each as `--attach '<file>#<caption>'` to
   `gh pr create` or `gh pr edit` (gh 2.99+; gh appends them to the body).
   Never commit them. If they could not be captured, open the PR as a draft
   and say why in the body.
8. **Learn.** `learner`, only when a stage looped, a reviewer found a real
   defect, or a human corrected the work. Proposals only; apply nothing.

## Small changes

One file and about 20 changed lines or fewer (tests and docs count): skip
stages 3 and 4 and subagents. Stages 1, 2, 5, 6 and 7 still run.

## Runner policy

The runner says whether web search is available. The repo's `AGENTS.md` or
the caller decides: commit, push and PR permissions; where proof is stored; extra gates (for example deploys needing
approval); and where Learn proposals go. When policy forbids a step, stop
before it and report. The human gate is PR review and merge.

## Result

Return a summary with:

- `criteria`: each criterion and its evidence (command, output, screenshot).
- `pr`: link, or why none was opened.
- `reviews`: plan review and code review verdicts and rounds used.
- `open_issues`: findings left after the round limits, or none.
- `lessons`: Learn proposals, or none.
