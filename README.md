# meta.cad.solidcraft

Shared documentation conventions and small templates for the BrainboxEmb
SolidCraft/CAD repository family. These conventions are **generic** across the
repositories listed below: a Python library, CLI tool, Docker image, CI
repository and CAD model repository can all use the same changelog guidance.

This is not an implementation repository, portfolio-wide policy system or
second issue tracker.

## Repositories in scope

The following repositories are covered by the shared *documentation* conventions.
The table records their responsibilities, not their live status, version pins
or dependency graph.

| Repository | Responsibility |
| --- | --- |
| [`lib.py.solidcraft.forge`](https://github.com/brainboxemb/lib.py.solidcraft.forge) | Forge Python CAD modeling API and compiler |
| [`lib.py.solidcraft.cmd`](https://github.com/brainboxemb/lib.py.solidcraft.cmd) | Thin Python facade for native SolidCraft commands |
| [`2026-011-02.cad.solidcraft`](https://github.com/brainboxemb/2026-011-02.cad.solidcraft) | Product/project CAD models and catalog |
| [`lib.py.cad.ci`](https://github.com/brainboxemb/lib.py.cad.ci) | Reusable CAD-CI engine and build logic |
| [`tool.cad.ci`](https://github.com/brainboxemb/tool.cad.ci) | Thin CAD-CI command/workflow adapter |
| [`tool.cad.ci.test`](https://github.com/brainboxemb/tool.cad.ci.test) | External acceptance of released CAD-CI |
| [`lib.py.cad.verification`](https://github.com/brainboxemb/lib.py.cad.verification) | Reusable CAD verification contracts/adapters |
| [`docker.cad.solidcraft`](https://github.com/brainboxemb/docker.cad.solidcraft) | Versioned SolidCraft and reference runtime images |
| [`tool.py.lib.ci`](https://github.com/brainboxemb/tool.py.lib.ci) | Generic Python library-CI tooling used by this family |
| [`tool.py.lib.ci.test`](https://github.com/brainboxemb/tool.py.lib.ci.test) | External acceptance for generic Python library CI |

"Covered" means these repositories can share documentation structure and
changelog guidance. It does **not** mean all ten use every template, that meta
owns their implementation, or that generic tooling becomes CAD-specific.

Additional repositories are included only by an explicit update to this list;
being owned by the same GitHub account alone is not sufficient.

## Shared templates

- [`templates/docs/plan.md`](templates/docs/plan.md) — structural guide
  for the current repository plan (`docs/plan.md`).
- [`templates/docs/handoff.md`](templates/docs/handoff.md) — structural guide
  for a session-entrypoint handoff (`docs/handoff.md`).
- [`templates/docs/CHANGELOG.md`](templates/docs/CHANGELOG.md) — generic release
  changelog structure and guidance for API, dependencies, infrastructure,
  internal implementation and documentation, with actual version/date history.

Use a template only when it fits the repository. Repository-specific facts,
release history, current plans and ownership decisions stay with the repository.

## Boundaries

This repository owns only small reusable documentation templates, shared
SolidCraft/CAD documentation conventions and descriptive cross-repository
metadata contracts (for example, a shared `model.yml` definition once agreed).

It does not own Forge, SCPC or product CAD implementations, CAD-CI/verification
execution, Docker runtimes, generated publications, Git/dependency tooling, or
generic portfolio governance. Their existing owner repositories remain
authoritative.

## Start here

- [`AGENTS.md`](AGENTS.md) — maintenance instructions and language rules.
- [`docs/plan.md`](docs/plan.md) — unfinished work in this meta repository.

Prefer links over copied policy and add a shared rule only when there is real
cross-repository need.
