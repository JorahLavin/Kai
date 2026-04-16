---
type: project-plan
project: claude-setup
last_updated: 2026-04-09
---

# Claude Setup — Reference Plan

**Context:** Set up Claude Code on Windows, connect Kai workspace to GitHub, and establish a reliable cross-device workflow so Claude can be used consistently across the Windows desktop and Linux laptop.

---

## Priority Reference — Full List

### Soon
| # | Item | Target Date | Notes |
|---|---|---|---|
| 1 | Install Claude Code on Windows | 2026-04-13 | Sunday session — block 2 hrs |
| 2 | Create private GitHub repo for working MT workspace | 2026-04-13 | Separate from Kerry Thompson template clone |
| 3 | Connect Windows MT folder to new GitHub repo | 2026-04-13 | Need to confirm whether folder already has .git |
| 4 | Verify `/open` → work → `/close` → auto-commit flow | 2026-04-13 | The core loop Kai is built around |

### Anytime — Quick Wins
| # | Item | Notes |
|---|---|---|
| 1 | Note Windows MT workspace folder path | Single folder path — needed before Sunday |
| 2 | Check whether MT folder already has a .git directory | Determines setup steps for GitHub connection |
| 3 | Add claude-setup as effort in SESSION.md | Drop these files into workspace on Sunday |

### Plan Ahead
| # | Item | Notes |
|---|---|---|
| 1 | Linux laptop workflow | After Windows/GitHub is stable — git pull + paste pattern |
| 2 | TRIGGERS.md entry for this effort | Add keywords once workspace structure is settled |
| 3 | Review Kai structure once Claude Code is live | First real `/open` session will surface any gaps |

---

## Key Facts and Constraints

- **Windows machine:** Primary development environment; Claude Code will live here
- **Linux laptop:** Secondary, used for breakfast/email sessions; no Claude Code planned
- **GitHub status:** Account is a few weeks old; currently only holds a clone of Kerry Thompson's public Kai repo — that is *not* the working workspace
- **Working MT files:** Location on Windows TBD — need folder path before Sunday setup
- **Time constraint:** Farmers market Saturday; Sunday is the first available setup window
- **Bandwidth:** ~45hr/week Wells Fargo + 9hr commute + household — setup must be low-friction once complete or it won't be used

---

## Decisions Already Made

- **GitHub is the sync layer** — not OneDrive, not Google Drive, not Obsidian Sync. Git handles text conflict resolution cleanly; the Kai `/close` workflow already commits and pushes.
- **Two repos, not one** — Kerry Thompson template clone stays as reference. A new private repo holds the working workspace.
- **Claude Code on Windows only (for now)** — Linux stays paste-based. Solve Windows first; Linux friction drops naturally once GitHub sync is live.
- **This project is a Kai effort** — tracked in the workspace like any other project. Self-referential but correct.

---

## Future / On Hold

- **Obsidian Sync** — Not needed if GitHub works. Revisit only if mobile access becomes a requirement.
- **Claude Code on Linux** — Not a priority; paste workflow is sufficient for breakfast sessions.
- **Full Kai customization for Rushbrook efforts** — Deferred until Claude Code is running and the basic loop is proven. Downstream efforts (Flask/Clearlight app, Excel recipe tool) wait on this foundation.
