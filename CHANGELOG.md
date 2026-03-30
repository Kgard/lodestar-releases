# Changelog

## [Unreleased]

### Added
- CLI: `lodestar init` — setup wizard with provider selection, API key validation, hook installation
- CLI: `lodestar start` / `save` / `end` — session lifecycle commands
- CLI: `lodestar review` — browser-based project dashboard
- CLI: `lodestar bootstrap` — capture existing project structure without LLM
- CLI: `lodestar summary` — 5-line session briefing for hooks/scripts
- CLI: `lodestar hooks` — git hook installation (auto-save on commit, full sync on push)
- MCP server: `lodestar_synthesize` and `lodestar_load` tools
- Providers: Anthropic, OpenAI, Google, Azure, Ollama
- Binary releases: macOS arm64, macOS x64, Linux x64, Windows x64
