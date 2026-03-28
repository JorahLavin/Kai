# MetaTemplate

A lightweight, file-based framework for working with AI on anything — projects, daily tracking, goals, or long-horizon work. Works with Claude Code, GitHub Copilot, M365 Copilot, or any AI with file access.

## What This Is

A small set of markdown files that give your AI assistant persistent context across sessions. Instead of re-explaining your work every time you open a chat, the AI reads a few files and picks up where you left off.

Works for any kind of effort: home improvement, software development, health tracking, daily task management, research, business planning — anything you want to work on consistently with AI assistance.

## How It Works

- `SESSION.md` — the AI reads this at the start of every session to orient itself
- `CONTEXT.md` — static background about you; loaded on demand, not every session
- `[effort]/project_plan.md` — stable goals and reference data for a project
- `[effort]/status.md` — current state: priorities, deadlines, what's active
- The AI updates `status.md` as you work, so the next session starts with accurate context

## Getting Started

See **[QUICKSTART.md](QUICKSTART.md)** for full setup instructions (under 15 minutes).

**Short version:**
1. Fork or download this repo and rename the folder (e.g. `my-workspace/`)
2. Fill in `SESSION.md` and `CONTEXT.md` with your name and first effort
3. Copy `_template/project_plan.md` and `_template/status.md` into a subfolder for your effort
4. Load `AGENT.md` in your AI tool and say "let's start"

## Repository Structure

```
├── AGENT.md              ← AI session instructions — load this in your AI tool
├── QUICKSTART.md         ← Full setup guide
├── SESSION.md            ← Fill in: your active efforts and immediate focus
├── CONTEXT.md            ← Fill in: who you are and how you work
├── _template/            ← Copy these to start a new effort
│   ├── project_plan.md
│   ├── status.md
│   ├── completed.md
│   ├── TRIGGERS.md       ← Keyword→file map for lazy loading (optional)
│   ├── PERSONAS.md       ← AI response modes per workstream (optional)
│   └── commands/         ← Copy to .claude/commands/ for Claude Code
│       ├── open.md
│       └── close.md
└── _meta/                ← Process docs and design decisions
    ├── PROCESS.md
    ├── DECISIONS.md
    ├── IMPROVEMENTS.md
    └── EXAMPLES.md
```

## Philosophy

- **Minimal setup** — one project name and a description is enough to start
- **AI-agnostic** — plain markdown files work with any AI tool
- **Persistent context** — the AI stays oriented across sessions without re-explaining
- **Evolves with use** — the template improves as you use it; `_meta/IMPROVEMENTS.md` captures lessons as they happen

## License

MIT
