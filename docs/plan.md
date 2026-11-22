# meta.cad.solidcraft repository plan

This file is the current source of truth for unfinished work in
`meta.cad.solidcraft`.

## Current accepted baseline

The repository exists as a deliberately small shared home for SolidCraft/CAD
conventions and templates.

Initial consumers:

- `brainboxemb/lib.py.solidcraft.forge`;
- `brainboxemb/2026-011-02.cad.solidcraft`.

No executable CI, verification, runtime or product-CAD implementation belongs
here.

## Active workstreams

### WS1 — shared repository documentation structure

Maintain small shared structural templates for:

- repository plans at `templates/docs/plan.md`;
- repository handoffs at `templates/docs/handoff.md`, consumed at
  `docs/handoff.md`.

The handoff is an entrypoint only. Current execution state remains in GitHub and
the consumer's `docs/plan.md`.

### WS2 — shared model-description contract

Forge #703 defines the canonical reusable `model.yml` description contract.
CAD #205 will adopt that contract once the owner decision is complete.

Keep this work descriptive only; build execution and generated verification
facts remain outside `model.yml`.

## Open issue assignment

| Issue | Repository | Status | Next action |
| --- | --- | --- | --- |
| #3 | meta | now | Accept the shared `docs/handoff.md` template/convention, then migrate Forge and CAD consumers. |
| #2 | meta | now | Continue coordination of tool.cad.ci API/architecture qualification without taking implementation ownership. |
| #1 | meta | now | Finish the shared Hugo-base decision before more CAD/Forge page divergence. |
| #205 | CAD | next | Adopt the canonical shared `model.yml` contract after Forge #703. |
| #204 | CAD | next | Remove derived SCPC command counts from model metadata. |
| #206 | CAD | later | Remove Forge-owned reference implementations from the product CAD repository. |

## Recently completed

- Created `meta.cad.solidcraft` as a narrow owner for shared CAD/SolidCraft
  conventions.
- Established explicit language rules for maintained engineering text.
- Established the shared repository-plan structure.

## Next checkpoint

Accept the shared handoff convention and prove it with Forge and
`2026-011-02.cad.solidcraft` as the first consumers, while keeping all current
repository status in their own plans.
