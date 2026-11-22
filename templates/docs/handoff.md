# <repository> handoff

Repository: `<repository>`.

Use this document only as the entrypoint for a new work session. Do not treat
copied handoff text as fresher than GitHub or `docs/plan.md`.

Before changing anything:

1. inspect the current issues, pull requests and branches;
2. read `AGENTS.md`;
3. read `docs/plan.md`;
4. treat `docs/plan.md` as the source of truth for unfinished work;
5. follow the repository's current issue/branch/PR discipline before implementation.

Shared SolidCraft/CAD documentation conventions live in
`brainboxemb/meta.cad.solidcraft`. Use
`templates/docs/plan.md` and `templates/docs/handoff.md` there as structural
references. Keep repository-specific work and status in this repository.

## Repository role

State the durable role of this repository in a few lines.

Include only ownership boundaries that help route work correctly. Do not copy
volatile implementation status from the plan.

## Durable working rules

Keep only rules that are expected to remain useful across work sessions, for
example:

- where generic behavior belongs when this repository is only a consumer;
- which permanent work lanes exist and what kind of work belongs on each;
- which merge entrypoint must be used;
- which local workaround must not be introduced.

Link to the owning repository or durable local documentation instead of
duplicating large policy sections.

## Start the next session

Tell the next agent which repository to inspect first, then explicitly require it
to derive the current execution order from live GitHub state and
`docs/plan.md`.

Do not put exact current SHAs, runtime/release pins, active issue/PR status,
temporary migration steps or "next four actions" here. Those facts belong in
GitHub and the repository plan and otherwise make the handoff stale.
