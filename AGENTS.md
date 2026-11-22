# Agent guidance

## Purpose

`meta.cad.solidcraft` is the small shared convention/template repository for
the BrainboxEmb SolidCraft/CAD repository family.

Keep it deliberately small. It documents shared structure; it does not become a
new implementation or orchestration layer.

## Start work

For every change:

1. read `README.md`;
2. read `docs/plan.md`;
3. inspect the consuming repositories affected by the convention;
4. change the smallest shared contract that solves the demonstrated drift;
5. keep implementation in the repository that owns that implementation.

## Language

Language use is a repository contract, not a per-file preference.

- Repository-maintained engineering text is written in **English**:
  README files, AGENTS files, plans, requirements, design documents, templates,
  issue titles/bodies, pull-request titles/bodies, commit messages and code
  comments.
- User/chat interaction follows the user's language. If the user writes Dutch,
  answer in Dutch.
- Do not mix Dutch and English prose inside one maintained engineering document.
- Keep established technical identifiers, API names, filenames and literal
  product/repository names unchanged; do not translate them.
- Literal quoted source text may remain in its original language.
- A deliberately user-facing document in another language is allowed only when
  its purpose explicitly requires that language. State that exception in the
  document.
- When normalizing an existing mixed-language shared template, prefer English;
  do not silently rewrite unrelated historical evidence merely for language
  consistency.

## Write simply

Use normal engineering language. Use the names that exist in the code and in
SolidCraft. Avoid architecture jargon and invented terms.

## Ownership boundary

This repository may own:

- shared SolidCraft/CAD documentation conventions;
- small reusable templates;
- cross-repository descriptive metadata contracts.

It must not own:

- executable CAD-CI or publication logic;
- Forge API/compiler code;
- verification execution;
- runtime/container code;
- product-model implementation;
- generic Git/dependency management;
- general BrainboxEmb portfolio governance.

Link to the owner repository instead of copying its implementation rules here.

## Plans

Every maintained repository in this SolidCraft/CAD family keeps its own current
plan document.

The shared structural reference is:

`templates/docs/plan.md`

A consumer plan contains repository-specific facts and work. Do not centralize
the consumers' current status in this repository.

The shared template defines structure only. It must not become a generated plan
engine or a second issue tracker.

## Changelogs

The shared, repository-type-neutral changelog structure and classification
guidance is in `templates/CHANGELOG.md`.

For each completed versioned release, record the real version and actual
release date in ISO `YYYY-MM-DD` form. `Unreleased` may remain undated.
Backfill old dates only from reliable release/tag evidence, not edit timestamps.

Distinguish the affected domain (public API/behavior, dependencies,
infrastructure/tooling, internal implementation, documentation) from the kind
of change (Added/Changed/Fixed/etc.). Use only meaningful nonempty domains.
Prioritize external impact and migration notes. Avoid duplicating entries,
inventing versions and turning a changelog into a commit log.

The covered repositories are listed explicitly in `README.md`; do not infer
scope from the account or repo prefix alone. Each consumer owns its actual
release notes and implementation.

Keep this a Markdown convention. Do not add changelog generators, validators or
CI enforcement without an independently accepted need.

## Handoffs

Every maintained repository in this SolidCraft/CAD family keeps its normal
handoff at:

`docs/handoff.md`

The shared structural reference is:

`templates/docs/handoff.md`

A handoff is an easy-to-find session entrypoint, not a second repository plan.
The document contains one clearly marked, complete copyable handoff-message
block. The surrounding prose only explains how to use or maintain that block.
The message must tell the next agent to inspect current GitHub state and then
read `AGENTS.md` and `docs/plan.md`.

Do not duplicate volatile state in a handoff: exact current SHAs,
runtime/release pins, active issue/PR status, temporary migration phases and
short-lived execution sequences belong in GitHub and `docs/plan.md`.

Repository-specific durable role and ownership boundaries may remain in the
consumer handoff when they help route work correctly.

## Change discipline

- One shared convention should have one clear owner here.
- Prefer links over duplicated policy text.
- Do not add tooling merely to enforce a convention that can remain a small,
  reviewable Markdown contract.
- Do not broaden a change from Forge/CAD into every repository unless evidence
  shows the convention is genuinely shared.
