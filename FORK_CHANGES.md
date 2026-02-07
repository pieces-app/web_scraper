# Fork Changes Documentation

This document tracks all custom modifications, patches, and deviations from the upstream `tusharojha/web_scraper` repository.

## Fork Information

- **Fork Repository**: `https://github.com/pieces-app/web_scraper`
- **Upstream Repository**: `https://github.com/tusharojha/web_scraper`
- **Current Branch**: `master`
- **Fork Version**: `0.1.4`
- **Commits Ahead**: 4
- **Commits Behind**: 0
- **Last Upstream Merge**: Fork is fully caught up with upstream

## Custom Modifications

### 1. Dependency Updates Only
- **Commits**: `e3ea26f`, `2ac8bae`, `e26934a`
- **Changes**:
  - Upgraded dependencies for SDK compatibility
  - Updated pubspec.yaml
- **Source Changes**: **NONE** -- no changes to `lib/` source code

### 2. Pubspec Update
- **Commit**: `e26934a`
- **Changes**: SDK constraint bumps

## Upstream Sync Status

- **Current Gap**: 0 commits behind (fully synced)
- **Status**: Fork only has dependency version bumps, no source code changes

## Why This Fork Exists

1. **SDK Compatibility**: Upstream may not have bumped SDK constraints as quickly as needed
2. **Workspace Integration**: Ensures compatibility with the pub workspace

## Future Considerations

1. **Consider Dropping Fork**: No source code changes; if upstream has compatible SDK constraints, this fork may be unnecessary
2. **Use `dependency_overrides`**: Could potentially override SDK constraints without maintaining a fork

## Contact

For questions about this fork or to request changes, contact the Pieces development team.
