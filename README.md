# meta.cad.solidcraft

Small shared convention repository for the BrainboxEmb SolidCraft/CAD
repository family.

Its job is deliberately narrow: keep a few shared documentation and metadata
contracts consistent across repositories such as:

- `lib.py.solidcraft.forge`;
- `2026-011-02.cad.solidcraft`;
- closely related SolidCraft/CAD owner repositories when a convention is
  genuinely shared.

## What belongs here

- small reusable documentation templates;
- the shared repository-plan structure;
- the shared repository-handoff structure;
- shared SolidCraft/CAD documentation conventions;
- shared descriptive metadata contracts such as the canonical `model.yml`
  contract once that contract is agreed.

## What does not belong here

This repository does not execute or implement:

- Forge API/compiler behavior;
- CAD-CI;
- verification engines;
- SolidCraft runtime/container packaging;
- Git/dependency tooling;
- product CAD models;
- portfolio-wide BrainboxEmb governance.

Those responsibilities stay in their owning repositories.

## Start here

- `AGENTS.md` — rules for maintaining this repository, including language use.
- `docs/plan.md` — current work in this repository.
- `templates/docs/plan.md` — shared structural template for repository plans.
- `templates/docs/handoff.md` — shared structural template for easy-to-find
  repository handoffs at `docs/handoff.md`.
- `templates/CHANGELOG.md` — shared changelog template; completed releases use
  both a version identifier and an ISO `YYYY-MM-DD` release date.

Keep this repository small. Add a shared rule only when at least two
SolidCraft/CAD repositories genuinely need the same convention.
