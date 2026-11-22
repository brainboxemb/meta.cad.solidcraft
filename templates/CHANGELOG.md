# Changelog

All notable changes to <repository> are recorded here.

Entries are ordered newest first.

## [Unreleased]

Record notable changes that have not been released yet.

Delete empty category headings. Use only the categories that help describe the
release, for example:

### Added

- <new behavior or capability>

### Changed

- <changed behavior or contract>

### Deprecated

- <deprecated behavior or API>

### Removed

- <removed behavior or API>

### Fixed

- <bug fix>

### Security

- <security-related change>

## [<version>] - YYYY-MM-DD

- <notable released change>

## Changelog rules

- Every completed release heading must contain both the version and the actual
  release date in ISO format: `## [<version>] - YYYY-MM-DD`.
- `[Unreleased]` is the only normal release section without a date.
- Keep releases in reverse chronological order, newest first.
- Use the repository's real released version identifier. Do not invent a
  version solely to satisfy the changelog format.
- Use the date on which that version was actually released. For historical
  entries, recover the date from the release/tag history or other reliable
  repository evidence; do not use the date on which the changelog was edited.
- Category headings such as `Added`, `Changed`, `Fixed`, `Removed`,
  `Deprecated` and `Security` are optional. Do not add empty headings.
- Keep entries concise and user- or maintainer-relevant. Detailed implementation
  history belongs in issues, pull requests and design documentation.
- A repository that does not publish versioned releases may adapt the release
  identifier, but dated accepted checkpoints must still use an unambiguous
  identifier plus an ISO date.
