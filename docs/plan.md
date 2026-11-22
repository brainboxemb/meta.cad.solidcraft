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

### WS1 — shared repository plan structure

Establish one small plan template and have Forge and the CAD product repository
reference the same structure without centralizing their actual work status.

### WS2 — shared model-description contract

Forge #703 defines the canonical reusable `model.yml` description contract.
CAD #205 will adopt that contract once the owner decision is complete.

Keep this work descriptive only; build execution and generated verification
facts remain outside `model.yml`.

## Open issue assignment

| Issue | Repository | Status | Next action |
| --- | --- | --- | --- |
| #707 | Forge | now | Link this repository from the Forge handoff and adopt the shared plan structure. |
| #205 | CAD | next | Adopt the canonical shared `model.yml` contract after Forge #703. |
| #204 | CAD | next | Remove derived SCPC command counts from model metadata. |
| #206 | CAD | later | Remove Forge-owned reference implementations from the product CAD repository. |

## Recently completed

- Created `meta.cad.solidcraft` as a narrow owner for shared CAD/SolidCraft
  conventions.
- Established explicit language rules for maintained engineering text.

## Next checkpoint

Prove the repository remains useful and small with only Forge and
`2026-011-02.cad.solidcraft` as initial consumers before adding more scope.
