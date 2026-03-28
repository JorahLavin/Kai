---
type: trigger-map
last_updated: YYYY-MM-DD
---

# Trigger Map

When [Your Name] references any of the following keywords or topics, load the corresponding file before responding. Do not load files proactively — only when the topic comes up.

| Keywords / Topics | File to Load |
|---|---|
| [keyword, keyword, keyword] | `[effort]/status.md` |
| planning, full list, road map, all projects | `[effort]/project_plan.md` |
| completed, finished, previously, archive | `[effort]/completed.md` |

*Add one row per effort. Keywords should be natural words you'd use in conversation — the AI matches on topic, not exact phrasing.*

---

## Adding a New Workstream

When you start a new workstream:

1. Add one row to the trigger table above (keywords → `status.md` path)
2. Create `[workstream]/status.md`, `[workstream]/project_plan.md`, `[workstream]/completed.md` from `_template/`
3. Add the workstream to `SESSION.md` Active Projects table
4. *(Claude Code only)* Create `.claude/commands/open[WorkstreamName].md` — explicit context injection skill
5. *(Claude Code only)* Add the new skill to the "Load a workstream" list in `.claude/commands/open.md`
