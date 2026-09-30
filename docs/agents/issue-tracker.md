# Issue tracker: GitHub

Issues and specs for this repo live in GitHub Issues at `k2htet/y-platform`. Use `gh` from this repository for issue operations.

## Conventions

- Create: `gh issue create --title "..." --body-file <file>`
- Read: `gh issue view <number> --comments`
- List: `gh issue list --state open --json number,title,body,labels,comments`
- Comment: `gh issue comment <number> --body-file <file>`
- Label: `gh issue edit <number> --add-label "..."` or `--remove-label "..."`
- Close: `gh issue close <number> --comment "..."`

When a skill says "publish to the issue tracker," create a GitHub issue. When it says "fetch the relevant ticket," read that issue and its comments. Use the label strings in `docs/agents/triage-labels.md`.

## Pull requests as a triage surface

**PRs as a request surface: no.** Set this to `yes` only if external PRs should enter the triage queue.

## Wayfinding operations

`/wayfinder` stores its map as one issue labelled `wayfinder:map` and its tickets as child issues. Link children with GitHub sub-issues when available; otherwise use a task list in the map and `Part of #<map>` in each child. Use `wayfinder:<type>` labels for research, prototype, grilling, and task tickets.

Represent blockers with native GitHub issue dependencies when available. Otherwise put `Blocked by: #<n>` at the top of the child issue. The next ticket is the first open, unassigned, unblocked child in map order. Claim it by assigning yourself. When resolved, record the answer in the child, close it, and add a short decision pointer to the map.
