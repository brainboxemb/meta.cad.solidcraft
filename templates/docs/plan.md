# <repository> plan

This file is the current source of truth for unfinished work in
`<repository>`.

Keep this file canonical on the repository's stable branch (`main` for the
current SolidCraft/CAD repositories). Normal and experimental lanes read the
stable plan. Their working-tree copies are synchronized projections and must
not become independent work queues.

Reconcile plan changes on a short-lived governance/docs branch created from the
stable branch and merge them back to stable through the repository's normal
merge policy. The one canonical plan describes all active lanes and workstreams.

State the repository's role in one short paragraph. Keep implementation history
in issues/change records rather than accumulating it here.

## Current accepted baseline

Record only the accepted state needed to understand current work:

- permanent source lanes or equivalent lifecycle branches;
- current accepted release/runtime/toolchain where relevant;
- important already-accepted architecture decisions;
- exact stable integration revision when that is operationally useful.

## Lane rule

Describe the repository's active work lanes and merge/promote rule.

Omit this section only when the repository genuinely has no lane distinction.

## Engineering constraints

When performance, feedback-loop cost or maintainability materially shapes the
repository, record the repository-specific constraints here and link to
`meta.cad.solidcraft/docs/engineering-principles.md` rather than copying the
shared principles. State only concrete local consequences or budgets.

Omit this section when those constraints are not material to current repository
architecture.

## Active workstreams

### WS1 — <name>

State:

- owner/lane;
- current status;
- next concrete gate;
- blockers or external owner work.

Add further workstreams only for genuinely independent current work.

## Open issue assignment

| Issue | Lane/owner | Status | Next action |
| --- | --- | --- | --- |
| #N | <lane> | now / next / later / blocked / probably obsolete / effectively complete but still open | <one concrete next action> |

Every open issue should be classifiable from this table or an explicitly linked
specialized tracker. Do not let the plan become a second issue-history log.

## Recently completed

Keep only a short recent context window that materially explains the current
baseline. Historical detail belongs in issues/change records.

## Next release/checkpoint

State the next real integration, release or acceptance checkpoint.

If the repository is not released, name the next equivalent acceptance gate.
