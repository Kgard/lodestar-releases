#![lodestar_demo_v3](https://github.com/user-attachments/assets/f63d4e9e-218b-441e-998d-e50e60ea5449)
 Lodestar

**The code is always saved. The thinking behind it wasn't. Now it is.**

Lodestar commits your reasoning to your repo — decisions, dead ends, and direction — and surfaces it in a single view so every session starts where the last one left off.

Built for founders who ship with AI. Works with Claude Code, Cursor, Windsurf, or whatever you use next.

> Kylex Module 00 · [kylex.io](https://kylex.io)

---

## Install

### npm (recommended)

```bash
npm install -g lodestar
```

### Homebrew

```bash
brew install lodestar
```

### Binary download

Download the latest release for your platform from [Releases](https://github.com/Kgard/lodestar-releases/releases).

| Platform | File |
|---|---|
| macOS (Apple Silicon) | `lodestar-macos-arm64.tar.gz` |
| macOS (Intel) | `lodestar-macos-x64.tar.gz` |
| Linux (x64) | `lodestar-linux-x64.tar.gz` |
| Windows (x64) | `lodestar-windows-x64.tar.gz` |

```bash
# Example: macOS Apple Silicon
curl -fsSL https://github.com/Kgard/lodestar-releases/releases/latest/download/lodestar-macos-arm64.tar.gz | tar xz
sudo mv lodestar lodestar-mcp /usr/local/bin/
```

### Verify checksums

Every release includes a `SHA256SUMS` file:

```bash
curl -fsSL https://github.com/Kgard/lodestar-releases/releases/latest/download/SHA256SUMS
sha256sum -c SHA256SUMS
```

---

## Quick start

```bash
cd ~/your-project
lodestar init         # One-time setup — provider, API key, hooks
```

That's it. Sessions are automatic after init:

| Event | What Lodestar does | Cost |
|---|---|---|
| You open your AI coding tool | Loads context + prints session summary | Free |
| You commit code | Updates feature progress | Free |
| You close your AI coding tool | Synthesizes session + commits context | ~$0.01 |

### Optional commands

```bash
lodestar save          # Mid-session checkpoint with optional notes
lodestar review        # Open project dashboard in browser
```

---

## What it captures

Lodestar synthesizes each session into a `.lodestar.md` file committed to your repo:

- **Decisions** — what was decided and why
- **Patterns** — naming and structural conventions established
- **Rejected approaches** — what was tried and why it didn't work
- **Open questions** — what's unresolved, and whether it's blocking
- **Next session** — where to pick up

Not a git log. A handoff note from a thoughtful colleague.

---

## How it works

1. **`lodestar init`** — one-time wizard: picks your AI provider, validates your API key, installs session hooks
2. **On session close** — reads git diffs, synthesizes context via your chosen LLM, writes `.lodestar.md`, commits it
3. **On session open** — reads `.lodestar.md`, prints a 5-line briefing, gives your AI tool full context

Your API key. Your repo. Your data stays local.

---

## CLAUDE.md vs .lodestar.md

> CLAUDE.md tells your tool how to behave. Lodestar tells it what already happened. You need both.

---

## Requirements

- Node.js 20+ (for npm install)
- Git
- An API key from Anthropic, OpenAI, Google, Azure, or a local Ollama instance

---

## License

Proprietary — Kylex LLC. See [LICENSE](LICENSE) for details.

---

Built by Kylex(https://kylex.io) · [Report an issue](https://github.com/Kgard/lodestar-releases/issues)
