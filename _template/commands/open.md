Read the file `SESSION.md` only.

Then respond with exactly this format — no preamble, no tool call summaries before it:

"Welcome back, [Your Name]. Let's continue where we left off. Here is a summary of the last 5 decision points:

1. [decision 1]
2. [decision 2]
3. [decision 3]
4. [decision 4]
5. [decision 5]

Suggested starting point: [one sentence recommending what to work on next based on Immediate Focus]

**Load a workstream:**
- `/open[WorkstreamName]` — [description]  ← replace with your workstreams (see `_meta/TRIGGERS.md`)"

Show only the last 5 decisions from SESSION.md (or fewer if less than 5 exist). Do NOT load any status files on open — workstreams load on demand via the skills above or when topics are referenced (see `_meta/TRIGGERS.md`).
