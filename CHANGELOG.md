# Changelog

All notable changes to the APICompass extension will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.1.3]

### Added

- Added `apicompass.enabled` workspace setting (default: `true`) to allow disabling APICompass per repository.

### Changed

- When `apicompass.enabled` is `false`, APICompass skips initial route scan and file watcher updates.
- Refresh, Search, and Export commands now show a clear message when APICompass is disabled for the workspace.
- Changing `apicompass.enabled` at runtime now applies immediately: enabling starts watchers and triggers a full scan; disabling stops watchers and clears cached routes.
- Sidebar empty state now shows a disabled-specific message when APICompass is disabled for the workspace.

## [0.1.2] - 2026-04-26

### Changed

- Updated repository and homepage URLs in package metadata.

## [0.1.1] - 2026-04-26

### Changed

- Updated Readme.

## [0.1.0] - 2026-04-26

### Added

- **Multi-framework route discovery** for Express.js, NestJS, Flask, Django, FastAPI, and Go (Gin, Echo, Chi, Fiber, net/http).
- **Interactive tree view** in the VS Code sidebar with collapsible groups by file, HTTP method, or framework.
- **Click-to-navigate** from any route directly to its source file and line number.
- **Real-time updates** via file watcher that re-parses changed files automatically.
- **Search** across all discovered routes by path, method, or file name.
- **Colour-coded icons** per HTTP method (GET green, POST blue, PUT orange, DELETE red, PATCH yellow).
- **Cross-file mount prefix resolution** for Express (`app.use`), Flask (`register_blueprint`), and FastAPI (`include_router`).
- **Same-file prefix resolution** for `app.use()`, `url_prefix`, and `include_router`.
- **Route deduplication** to remove exact duplicates when multiple parsers match the same file.
- **Export** all routes to JSON or OpenAPI 3.0 (YAML/JSON).
- **Keyboard shortcuts**: `Ctrl+Shift+A R` to refresh, `Ctrl+Shift+A S` to search.
- **Context menus**: right-click a route to copy its path or a cURL command.
- **Configurable** include/exclude paths, enabled frameworks, and grouping style via VS Code settings.
