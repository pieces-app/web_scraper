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

## Evaluation: Can This Fork Be Dropped? (February 2026)

**Result: NO -- keep the fork.**

Despite having zero source code changes (`git diff upstream/master..HEAD -- lib/` is empty), the fork cannot be dropped because:

1. **Pub.dev SDK constraint is incompatible**: The upstream pub.dev version (0.1.4) has SDK constraint `>=2.12.0-259.12.beta <3.0.0` -- this is **incompatible with Dart 3.6**.
2. **Dependency versions are incompatible**: Upstream uses `http: ^0.13.0` (Dart 2 era). Our fork bumps to `http: ^1.1.2` (Dart 3 compatible).
3. **Upstream is stale**: Last push Jun 2024, 25 open issues, no maintainer activity. Unlikely to get SDK bump from upstream.
4. **Workspace integration**: Fork has `resolution: workspace` for pub workspace compatibility.

## Why This Fork Exists

1. **SDK Compatibility**: Upstream pub.dev version uses `<3.0.0` SDK constraint. Fork bumps to `>=3.6.0 <4.0.0`.
2. **Dependency Compatibility**: Fork updates `http` from `^0.13.0` to `^1.1.2` and `html` from `^0.15.0` to `^0.15.4`.
3. **Workspace Integration**: Ensures compatibility with the pub workspace via `resolution: workspace`.

## Future Considerations

1. **Monitor Upstream**: If upstream ever bumps SDK constraints to Dart 3+, the fork can be dropped immediately (zero source changes).
2. **Alternative Package**: Evaluate if `dart_web_scraper` or another maintained package could replace `web_scraper`.
3. **Upstream is effectively abandoned**: 25 open issues, no recent activity. Consider this fork permanent unless an alternative package is adopted.

## Contact

For questions about this fork or to request changes, contact the Pieces development team.
