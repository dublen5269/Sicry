# Changelog

All notable changes to SICRY™ are documented here.

Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
Versioning follows [Semantic Versioning](https://semver.org).

---

## [1.0.0] — 2026-03-14

### Added
- 18 dark web search engines (14 .onion engines + 4 clearnet Tor-routed fallbacks)
- 6 agent tools: `search`, `fetch`, `check_tor`, `renew_identity`, `ask`, `dispatch`
- Native tool schemas for Anthropic, OpenAI, and Gemini
- FastMCP server (`python3 sicry.py serve`)
- 4 LLM analysis modes: `summary`, `entity`, `threat`, `ioc`
- Full Robin OSINT pipeline baked in — no separate Robin install needed
- Tor authentication: cookie, password, hash, and unauthenticated fallback
- `__version__ = "1.0.0"`
- GitHub Actions CI (Python 3.9–3.12)
- `CONTRIBUTING.md`, `SECURITY.md`, issue templates

### Fixed
- URL extraction now includes clearnet fallback when no `.onion` links found (fixes DuckDuckGo-Tor / Ahmia-clearnet returning 0 results)
- Ahmia `/redirect/?redirect_url=` wrapper decoded correctly
- CSS selector result containers targeted before falling back to all `<a>` tags
- `ANTHROPIC_MODEL` corrected to `claude-opus-4-5`
- Unclosed file handle in `renew_identity()` replaced with `with open()` block

---

<!-- next release goes here
## [Unreleased]
### Added
### Changed
### Fixed
### Removed
-->

[1.0.0]: https://github.com/JacobJandon/Sicry/releases/tag/v1.0.0
