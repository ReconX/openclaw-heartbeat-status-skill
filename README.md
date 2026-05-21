# Heartbeat status skill

Lightweight OpenClaw skill that adds a **heartbeat routine** to HEARTBEAT.md. Each run it:

1. **Reports status** — session count (via `sessions_list`) and current time.
2. **Stays up to date** — runs `git pull` in the skill directory and, if `CHANGELOG.md` exists, reads the latest entry and applies any configuration or procedure updates described there.

So you get a useful status check and the skill can evolve via changelog without you re-running setup. See `SKILL.md` for the skill contract.

---

## Setup

Add the section below to `HEARTBEAT.md` (with the user's confirmation). No URLs in HEARTBEAT — only a reference to the local routine file that ships with this repo.

**Section to add** (use the path where this repo was cloned, e.g. `openclaw-heartbeat-status-skill`):

```
## Heartbeat status
- Each heartbeat: run the steps in openclaw-heartbeat-status-skill/HEARTBEAT_ROUTINE.md
```

Replace `openclaw-heartbeat-status-skill` with the actual folder name if you cloned it elsewhere.

---

## License

MIT
