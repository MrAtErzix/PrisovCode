<pre align="center">
█▀▀█ █▀▀█ ▀▀▀▀ █▀▀▀ █▀▀█ █  █ █▀▀▀ █▀▀█ █▀▀▄ █▀▀
█▀▀▀ █▀▀▄   █  ▀▀▀▄ █  █  ██. █    █  █ █  █ █▀▀
█    █  █ ▀▀▀▀ ▀▀▀▀ ▀▀▀▀   █. ▀▀▀▀ ▀▀▀▀ ▀▀▀  ▀▀▀
</pre>

<h3 align="center">The AI Agent That Lives in Your Terminal</h3>

<p align="center">
  <b>Analyze • Write • Refactor • Debug — All Without Leaving the CLI</b>
</p>

<p align="center">
  <a href="https://github.com/MrAtErzix/PrisovCode/releases"><img alt="GitHub release" src="https://img.shields.io/github/v/release/MrAtErzix/PrisovCode?style=flat-square&label=version" /></a>
  <a href="https://github.com/MrAtErzix/PrisovCode/stargazers"><img alt="GitHub stars" src="https://img.shields.io/github/stars/MrAtErzix/PrisovCode?style=flat-square&label=stars" /></a>
  <a href="https://github.com/MrAtErzix/PrisovCode/blob/dev/LICENSE"><img alt="License" src="https://img.shields.io/github/license/MrAtErzix/PrisovCode?style=flat-square" /></a>
  <a href="https://github.com/MrAtErzix/PrisovCode/actions"><img alt="Build status" src="https://img.shields.io/github/actions/workflow/status/MrAtErzix/PrisovCode/publish.yml?style=flat-square&branch=dev" /></a>
  <img alt="Platform" src="https://img.shields.io/badge/platform-linux%20%7C%20macOS%20%7C%20windows-blue?style=flat-square" />
</p>

<br>

![PrisovCode Terminal UI](packages/web/src/assets/lander/screenshot.png)

---

## ✨ What is PrisovCode?

**PrisovCode** is an open-source AI-powered development agent that runs natively in your terminal. It understands your entire project context — code, git history, file structure — and helps you build software faster.

Think of it as an AI pair programmer that actually uses your tools: it edits files, runs shell commands, searches code, works with git, and supports **15+ LLM providers** — all from the command line.

```
PrisovCode needs to add authentication middleware:

  Analyzing codebase structure...
  Reading src/middleware/auth.ts...
  Reading src/routes/api.ts...
  Adding JWT verification to all /api/* routes ✓
  Running tests... ✓
```

---

## 🚀 One-Line Install

### Linux & macOS
```bash
curl -fsSL https://github.com/MrAtErzix/PrisovCode/releases/latest/download/install.sh | bash
```

### Windows (PowerShell)
```powershell
iwr -Uri "https://github.com/MrAtErzix/PrisovCode/releases/latest/download/install.ps1" -UseBasicParsing | iex
```

---

## 📦 Package Managers

| Platform | Command |
|----------|---------|
| **Any (npm)** | `npm i -g prisovcode` |
| **macOS (Homebrew)** | `brew install MrAtErzix/tap/prisovcode` |
| **Windows (Scoop)** | `scoop bucket add prisovcode https://github.com/MrAtErzix/scoop-prisovcode && scoop install prisovcode` |
| **Windows (Choco)** | `choco install prisovcode` |
| **Arch Linux** | `yay -S prisovcode-bin` |
| **Nix (any OS)** | `nix run github:MrAtErzix/PrisovCode` |

### Direct Download (any Linux distro)

For Debian, Ubuntu, Fedora, or any other distribution — grab the prebuilt binary directly:

```bash
curl -LO https://github.com/MrAtErzix/PrisovCode/releases/latest/download/prisovcode-linux-x64.tar.gz
tar -xzf prisovcode-linux-x64.tar.gz
sudo mv prisovcode /usr/local/bin/
```

Or with wget:

```bash
wget https://github.com/MrAtErzix/PrisovCode/releases/latest/download/prisovcode-linux-x64.tar.gz
tar -xzf prisovcode-linux-x64.tar.gz
sudo mv prisovcode /usr/local/bin/
```

Available variants: `linux-x64`, `linux-x64-baseline` (no AVX2), `linux-arm64`, `linux-x64-musl`, `linux-arm64-musl`, `darwin-arm64`, `darwin-x64`, `win32-x64`, `win32-arm64`.

### Desktop App (BETA)

| Platform | Format |
|----------|--------|
| **Debian / Ubuntu** | `.deb` — [Download latest](https://github.com/MrAtErzix/PrisovCode/releases/latest) |
| **Fedora / RHEL** | `.rpm` — [Download latest](https://github.com/MrAtErzix/PrisovCode/releases/latest) |
| **Any Linux** | `.AppImage` — [Download latest](https://github.com/MrAtErzix/PrisovCode/releases/latest) |
| **macOS** | `.dmg` — [Download latest](https://github.com/MrAtErzix/PrisovCode/releases/latest) |
| **Windows** | `.exe` — [Download latest](https://github.com/MrAtErzix/PrisovCode/releases/latest) |

---

## 🔧 Build from Source

Requires [Bun](https://bun.sh) (v1.3+):

```bash
git clone git@github.com:MrAtErzix/PrisovCode.git
cd PrisovCode
bun install
bun run packages/opencode/script/build.ts --single
```

The binary will be at `packages/opencode/dist/`.

---

## ⚡ Quick Start

```bash
# Launch TUI in current directory
prisovcode

# Open a specific project
prisovcode /path/to/project

# Choose provider and model
prisovcode --provider anthropic --model claude-sonnet-4-20250514

# Start as an API server
prisovcode serve

# Open web interface
prisovcode web

# Help & commands
prisovcode --help
```

On first launch, PrisovCode will walk you through API key setup.

### Commands Overview

| Command | Description |
|---------|-------------|
| `prisovcode` | Launch terminal UI |
| `prisovcode run` | Execute a one-shot task |
| `prisovcode serve` | Start HTTP API server |
| `prisovcode web` | Open browser UI |
| `prisovcode agent` | Manage agents |
| `prisovcode providers` | Configure LLM providers |
| `prisovcode upgrade` | Update to latest version |
| `prisovcode uninstall` | Remove PrisovCode |

---

## 🧠 Built-in Agents

Switch between agents with the `Tab` key:

| Agent | Description |
|-------|-------------|
| **build** | Full-access: edit code, run commands, install packages |
| **plan** | Read-only: analyze code, plan changes, ask questions |
| **@general** | Sub-agent: complex searches, multi-step tasks |

---

## ⚙️ Configuration

Create a `prisovcode.json` in your project root or `~/.config/prisovcode/prisovcode.json`:

```json
{
  "provider": "anthropic",
  "model": "claude-sonnet-4-20250514",
  "agent": "build",
  "permissions": {
    "allow": ["bash", "file", "search"],
    "deny": []
  }
}
```

---

## 🌟 Features

- **15+ LLM Providers** — OpenAI, Anthropic, Google, Mistral, Groq, Azure, AWS Bedrock, Perplexity, OpenRouter, GitHub Copilot, DeepSeek, TogetherAI, Cerebras, DeepInfra, xAI, Cohere and more
- **MCP & ACP** — Model Context Protocol & Agent Communication Protocol support
- **Plugin System** — SDK for writing custom plugins
- **VS Code Extension** — Use PrisovCode from your editor
- **Web & Desktop** — Full-featured Electron app included
- **Permission System** — Granular allow/deny rules, read-only modes
- **Tree-sitter Parsing** — Syntax-aware code understanding for 10+ languages
- **Terminal UI** — Beautiful TUI built with SolidJS + OpenTUI
- **Docker Support** — Ready-to-use containers

---

## 🛠 Development

```bash
git clone git@github.com:MrAtErzix/PrisovCode.git
cd PrisovCode
bun install
bun dev                    # Dev mode with hot reload
bun dev -- /path/to/proj   # With a specific project
bun lint                   # Oxlint
```

---

## 📄 License

MIT © PrisovCode

---

<p align="center">
  <a href="https://github.com/MrAtErzix/PrisovCode">GitHub</a> •
  <a href="https://github.com/MrAtErzix/PrisovCode/releases">Releases</a> •
  <a href="https://github.com/MrAtErzix/PrisovCode/issues">Issues</a> •
  <a href="https://github.com/MrAtErzix/PrisovCode/discussions">Discussions</a>
</p>
