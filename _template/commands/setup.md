You are helping a new user set up their AI-assisted workspace for the first time. Guide them through setup conversationally — one question at a time. Do not ask multiple questions at once. Be warm and brief.

## Setup Flow

Ask these questions in order. Wait for each answer before asking the next.

1. "What's your name?" *(used to personalize the session greeting)*
2. "What's the first thing you want to track with AI? This can be anything — a home project, work goals, health, a hobby, a business idea." *(this becomes their first effort)*
3. "Give me one sentence describing it." *(goes in project_plan.md)*
4. "What are you working on right now, or what do you want to focus on first?" *(becomes Immediate Focus in SESSION.md)*
5. "Anything about yourself or how you like to work that would help the AI? For example: your job, how direct you want responses, anything to avoid. Skip if you're not sure." *(goes in CONTEXT.md — if they skip, use a placeholder)*

## After Collecting Answers

Write the following files without asking for further confirmation. Tell the user what you're doing as you go.

### CLAUDE.md
Copy the full contents of `AGENT.md` into `CLAUDE.md`. Replace `[Your Name]` with their name throughout.

### SESSION.md
Write a fresh `SESSION.md` using this structure:
```
---
type: session-loader
last_updated: [today's date]
---

# Session Loader

## Active Projects

| Project | Status Files | Priority |
|---|---|---|
| [effort name] | `[effort-folder]/project_plan.md`, `[effort-folder]/status.md` | HIGH |

## Immediate Focus
- [their answer to question 4]

## Last Session Decisions
*(none yet — fills in after first close)*
```

Use a short folder name for the effort (lowercase, hyphenated, e.g. "home-project", "work-goals").

### CONTEXT.md
Write a fresh `CONTEXT.md` using this structure:
```
---
type: static-context
last_updated: [today's date]
---

# Static Context

*Load on demand — not every session.*

---

## About You
- [their name], using this workspace to track: [effort name]
- [their answer to question 5, or "No additional context provided yet."]

---

## Purpose of This Workspace
[their one-sentence description from question 3]

---

## Active Efforts

| Effort | Scope | Files |
|---|---|---|
| [effort name] | [one-sentence description] | `[effort-folder]/` |

---

## File Map
\```
[workspace]/
├── CLAUDE.md / AGENT.md    ← AI behavior instructions
├── SESSION.md              ← pointer table + immediate focus
├── CONTEXT.md              ← this file — static context
├── [effort-folder]/
│   ├── project_plan.md
│   └── status.md
└── _template/              ← blank files for new efforts
\```
```

### .claude/commands/open.md
Replace `[Your Name]` with their name. Remove the workstream list placeholder line — they have no workstreams yet. The file should end after the suggested starting point line.

### Effort folder
Create `[effort-folder]/` and copy `_template/project_plan.md` and `_template/status.md` into it. Fill in the effort name and description. Leave the rest for them to build out.

## Confirm

When all files are written, respond with:

"You're all set, [name]. Type `/open` to start your first session."
