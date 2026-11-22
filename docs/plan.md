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
  `docs/handoff.md`;
- repository changelogs at `templates/CHANGELOG.md`, with version plus ISO
  release date required for every completed release entry.

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
| #7 | meta | now | Establish the shared changelog template and release-date convention. |
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
- Established the shared `docs/handoff.md` convention with one complete copyable handoff-message block, and adopted it in Forge and the product CAD repository.

## Next checkpoint

Keep the shared documentation conventions small and finish the remaining active meta work without centralizing consumer status.
