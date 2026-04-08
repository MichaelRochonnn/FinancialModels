# Changelog

All notable changes to this repository will be documented in this file.

This project currently uses a lightweight, date-based changelog until a formal versioning scheme is introduced.

## [Unreleased]

### Added

- Added `docs/assets/favicon.svg` and configured it as the docs site favicon.
- Added CTA sections and landing-page style content blocks to `docs/index.md`.

### Changed

- Fixed the MkDocs strict build by excluding `docs/README.md` from the generated site and converting repo-root/example references to GitHub URLs.
- Updated the docs workflow to call MkDocs through `python -m mkdocs`, which is more robust on GitHub Actions runners.
- Refined `docs/stylesheets/extra.css` with landing-page layout styles for CTA, cards, and responsive sections.
- Reverted the unsupported automatic Pages enablement attempt in the workflow and documented the required first-time manual Pages setup step.
- Upgraded `mkdocs.yml` with grouped navigation, footer navigation, social links, font settings, dark-mode toggle, and richer Material theme features.
- Updated the top-level `README.md` to reflect the expanded docs-site structure and styling layer.

## [2026-04-08]

### Added

- Added `docs/assets/hero-banner.svg` as a reusable visual cover for the repository and docs pages.
- Added `mkdocs.yml` and a GitHub Pages workflow so the docs can be deployed as a lightweight site.
- Added `docs/index.md` as a dedicated MkDocs home page.
- Added `docs/assets/` with SVG workflow diagrams for usage flow, model routing, and output structure.
- Added visual sections to the docs pages so the repository reads more like a compact documentation site.
- Added a `docs/` directory with installation guidance, a Chinese usage guide, and sample output documentation.
- Added `.github/CODEOWNERS` to define the default repository owner.
- Added `CHANGELOG.md` to track project-level changes over time.
- Added `financial-modeling-suite`, a 12-model Codex skill for valuation, modeling, scenario analysis, and investment-committee style outputs.
- Added `financial-modeling-quickstart`, a conversational front door for short prompts such as `跑 DCF` and `做个三张表`.
- Added a formal English `README.md` describing installation, invocation, examples, and repository structure.
- Added `examples/` documentation for invocation patterns, input templates, and release checklist guidance.
- Added `LICENSE` under the MIT License.
- Added `CONTRIBUTING.md` with repository-specific guidance for skill contributions and validation.
- Added `SECURITY.md` with a lightweight security reporting policy.
- Added GitHub community health files including issue templates and a pull request template.
