# <repository> handoff

Repository: `<repository>`.

This document is the easy-to-find handoff entrypoint for a new work session.
It contains one copyable handoff message below.

The handoff message is deliberately an entrypoint, not a second repository
plan. Current work must always be derived from live GitHub state and the
canonical stable-branch `docs/plan.md` (normally `main`).

Shared SolidCraft/CAD documentation conventions live in
`brainboxemb/meta.cad.solidcraft`. Use
`templates/docs/plan.md` and `templates/docs/handoff.md` there as structural
references.

## Handoff message

Copy the complete text block below into a new chat.

~~~text
You are continuing work on <repository>.

Repository role:

- <durable repository responsibility>;
- <important ownership boundary>;
- <important related owner repositories when needed>.

Use this handoff only as the entrypoint. Do not treat copied handoff text as
fresher than GitHub or the repository plan.

Start by:

1. inspecting the current issues, pull requests and branches;
2. reading AGENTS.md;
3. reading the canonical stable-branch docs/plan.md (normally main);
4. treating that stable docs/plan.md as the source of truth for unfinished work;
5. following the current work order from the plan rather than from old handoff
   text;
6. creating an issue before implementation when the logical change has none;
7. keeping one logical change to one issue, branch and PR;
8. updating requirements/design documentation when behavior or architecture
   changes;
9. reconciling the plan after merge or release.

Durable working rules:

- <rule that remains useful across sessions>;
- <owner boundary that prevents a local workaround>;
- <lane or merge rule only when it is genuinely durable>;
- reconcile docs/plan.md on the stable branch; development-lane copies are
  synchronized projections, not independent plans.

Shared document structures live in brainboxemb/meta.cad.solidcraft:
templates/docs/plan.md and templates/docs/handoff.md.

Do not copy exact current SHAs, runtime/release pins, active issue/PR status,
temporary migration phases or a short-lived "next actions" list into this
handoff. Those facts belong in GitHub and docs/plan.md.
~~~

## Template guidance

The text block above is the actual handoff message.

Everything outside that block only explains how to use or maintain the
document. A consumer may translate the copyable message to the user's normal
chat language when that is intentional; repository-maintained explanatory text
outside the block remains English.

Keep repository-specific durable role and ownership guidance in the block when
it helps route work correctly. Do not turn the handoff into a status snapshot.
