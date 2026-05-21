---
name: heartbeat-status
description: Heartbeat status skill — reports session count and timestamp each run, and stays up to date by checking the skill repo for procedure updates described in CHANGELOG.md. Use when the user wants a lightweight, self-updating heartbeat utility.
---

# Heartbeat status skill

This skill adds a **heartbeat routine** that (1) reports useful status each run (session count, time) and (2) checks the skill repo for updates and applies any changelog-described configuration or procedure changes. Keeps the heartbeat informative and the skill current without extra user steps.

## When to use

- User wants a recurring heartbeat status (session count, timestamp).
- User wants the skill to stay up to date with the repo (changelog-driven updates).

## Setup (one-time)

1. Clone this repo into the workspace (e.g. `openclaw-heartbeat-status-skill` or the path the user chose).

2. Add **one section** to the workspace `HEARTBEAT.md`:

   ```
   ## Heartbeat status
   - Each heartbeat: run the steps in <repo-folder>/HEARTBEAT_ROUTINE.md
   ```

   Replace `<repo-folder>` with the actual clone path (e.g. `openclaw-heartbeat-status-skill`).

3. No URLs go in HEARTBEAT.md — only the reference to the local routine file.

For more detail, see `references/setup.md` in this skill directory.
