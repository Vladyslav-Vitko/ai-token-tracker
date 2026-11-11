# Changelog

All notable changes to **AI Token & Cost Tracker** are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.2] - 2026-11-11

### Added
- **licensing:** Introduce multi-tier subscriptions, background re-validation, and pricing selector.

### Changed
- **licensing, web:** Enforce UTC date bounds, badges, and add v1.1.1 changelog link.
- **web:** Standardize API Console button and add dynamic green/gold license styling.
- **ui, licensing:** Remove pseudo-quota labels, hide Pro badges for licensed tier, and elevate copy.
- **web:** Refine Pro badge design, soften upgrade notices.
- **vscode-ext:** Eliminate uppercase shouting and modernize status bar and dialog copywriting.
- **web, changelog:** Elevate table empty states copy and align changelog version SSoT.
- **web:** Modernize modal dialog copywriting and bilingual localization.
- **web, docs:** Modernize dashboard copywriting, bilingual localization, and documentation formatting.
- **vscode-ext:** Modernize quick pick menu copy and localization standards.


## [1.1.0] - 2026-11-09

### Added

- **vscode-ext, backend:** Add universal Multi-Extension AI Chat Plan & Session tracking (`PlanProviderAdapter`) for VS Code, VSCodium, and Windsurf (`google.google-antigravity`, `github.copilot-chat`, `anthropic.claude-code`, `openai.chatgpt`, `saoudrizwan.claude-dev` / `rooveterinaryinc.roo-cline` / `kilocode.kilo-code`, `continue.continue`) with combined `all` view and per-extension switcher.
- **plan-ingestor:** Enable deterministic token estimation (`is_estimated = 1`, `include_legacy_estimated_by_default: true`) by default alongside exact usage counters so status bar and Tab 1 charts never render empty for chat-only extensions.

## [1.0.2] - 2026-11-08

### Added

- **release:** Add automated multi-registry release pipeline and unify version SSoT.

### Fixed

- **backend, vscode-ext:** Eliminate file descriptor leaks and harden daemon lifecycle.

### Documentation

- **release:** Clarify Azure DevOps organization and VSCE_PAT setup steps in .env.release.example.

## [1.0.1] - 2026-11-07

### Added

- Zero-config self-contained backend auto-start on IDE startup with automatic Python 3 (`>= 3.10`) interpreter discovery and interactive interpreter selector (`aiTokenTracker.selectPython`).
- Integrated extension & daemon diagnostics output channel (`aiTokenTracker.showLogs`).
- Embedded full stdlib Python backend inside `.vsix` (`extension/backend/`) for standalone Marketplace and Open VSX installations.

### Fixed

- Escaped XML entities in `extension.vsixmanifest` and enforced strict Open Packaging Conventions (`[Content_Types].xml`) schema compliance.
- Rewrote relative repository image and documentation links to HTTPS URLs inside packaged `.vsix` archives for VS Code Marketplace and Open VSX rendering.
- Aligned Marketplace extension identifier (`VladyslavVitko.ai-token-cost-tracker`) across manifest, installer, and documentation.

## [1.0.0] - 2026-11-04

### Added

- Initial release of **AI Token & Cost Tracker** featuring the local Dual-Ledger Architecture (`127.0.0.1:8787`).
- Multi-Provider Paid LLM API Gateway supporting Google Gemini (incl. Gemini 4 Argon), Anthropic Claude, OpenAI, OpenRouter, and custom OpenAI/Anthropic-compatible endpoints.
- Strict IDE-isolated Subscription Plan analytics (`$0.00` extra cost) for Antigravity IDE and Cursor IDE via lifecycle hooks, transcript ingestion, and Cursor CSV import.
- Hardware-style Paid API safety switch (`LOCKED` by default), daily/monthly USD budget circuit breakers, and `chmod 0600` secret storage.
- Adaptive WCAG 2.2 AA / WAI-ARIA Dual-Tab Web Dashboard (`<dialog>`, Popover API, CSS `@container` queries) with full English and German (`EN` / `DE`) localization.

[1.1.2]: https://github.com/Vladyslav-Vitko/ai-token-tracker/compare/v1.1.0...v1.1.2

[1.1.0]: https://github.com/Vladyslav-Vitko/ai-token-tracker/compare/v1.0.2...v1.1.0
[1.0.2]: https://github.com/Vladyslav-Vitko/ai-token-tracker/compare/v1.0.1...v1.0.2
[1.0.1]: https://github.com/Vladyslav-Vitko/ai-token-tracker/compare/v1.0.0...v1.0.1
[1.0.0]: https://github.com/Vladyslav-Vitko/ai-token-tracker/releases/tag/v1.0.0
