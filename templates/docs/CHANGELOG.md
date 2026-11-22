# Changelog

Notable changes to <repository>, newest first.

## [Unreleased]

### Public API and behavior

- **Added:** <new supported capability or externally visible behavior>.

### Dependencies and compatibility

- **Changed:** <dependency from version A to version B; reason, and any
  required migration or compatibility impact>.

### Infrastructure and tooling

- **Changed:** <build, packaging, CI, publication or development-tool change;
  state whether users are affected>.

### Internal implementation

- **Fixed:** <significant internal correction worth recording; omit routine
  refactoring without an observable or maintainer-relevant outcome>.

### Documentation

- **Added:** <important guide, reference or documentation update>.

## [<version>] - YYYY-MM-DD

### Public API and behavior

- **Fixed:** <resolved public issue and its observable effect>.

## Changelog guidance

Use this file as a structural example, not a list of headings that must always
appear. Remove placeholders and empty sections. Complete releases require
`## [<version>] - YYYY-MM-DD` using the **actual release date**; only
`[Unreleased]` is normally undated. Keep versions newest first. For past
releases, verify dates from tags/releases or other reliable repository evidence;
never substitute the changelog edit date.

Classify by the area impacted (section), then the kind of change (bold prefix,
when useful). These are separate dimensions: an API fix belongs under
`Public API and behavior`, while a dependency update belongs under
`Dependencies and compatibility`, even if both are technically "Changed".
Use `Added`, `Changed`, `Deprecated`, `Removed`, `Fixed` or `Security`
as prefixes when they improve clarity; do not force one for every entry.

- **Public API and behavior:** externally supported functions, signatures,
  commands, model contracts, outputs, compatibility and breaking changes.
  Name the affected symbol/behavior; give migration instructions when needed.
- **Dependencies and compatibility:** added, upgraded, replaced or removed
  libraries, runtimes, engines or supported versions. State the old/new
  dependency when relevant, and whether users must change pins or configuration.
  Do not treat every lockfile-only/no-impact update as release news.
- **Infrastructure and tooling:** CI, workflows, build/release systems,
  packaging, containers, generated websites and developer tools. Mention
  user-visible effects when they exist; otherwise mark the effect as internal.
- **Internal implementation:** meaningful refactors, performance, correctness
  and architecture changes that do not alter the public contract. Routine
  maintenance may be omitted.
- **Documentation:** substantial guides, examples or reference improvements;
  do not list each typo or formatting change.

One change should normally have **one primary entry** in its most meaningful
section. If a dependency upgrade also changes the public API, describe the
public impact first and refer to the dependency there or add a short
cross-reference; do not duplicate the same paragraph. Put important migration
or breaking-change information before minor maintenance details.

Write outcomes and impact rather than a commit log. Include issue/PR links when
they make follow-up useful. Preserve truthful past release history. A repository
without versioned releases can use an unambiguous accepted-checkpoint
identifier plus an ISO date; do not invent release versions.
