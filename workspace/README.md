# Workspace (household template)

This directory is the **copyable household workspace** for Tradclaw: OpenClaw bootstrap files plus `resources/` for structured household notes.

**OpenClaw vocabulary:** what is official vs Tradclaw-only is summarized in [`../tradclaw/openclaw-primitives.md`](../tradclaw/openclaw-primitives.md) (workspace file map, memory, heartbeat, skills precedence, `BOOTSTRAP.md` vs `tradclaw/BOOTSTRAP.md`).

## Using it with OpenClaw

1. Complete the interview and module selection using [`../tradclaw/BOOTSTRAP.md`](../tradclaw/BOOTSTRAP.md).  
2. Merge or copy these files into your real OpenClaw workspace (often the workspace root where `AGENTS.md` and `SOUL.md` live).  
3. Keep **optional** automation in the repo’s [`../skills/`](../skills/) and [`../cron/`](../cron/) folders — install or schedule only what you chose.

## Layout

- **OpenClaw bootstrap files:** `AGENTS.md`, `SOUL.md`, `IDENTITY.md`, `USER.md`, `TOOLS.md`, `HEARTBEAT.md`, `MEMORY.md` (optional but recommended for households)  
- **Daily memory:** `memory/` — `YYYY-MM-DD.md` per [Memory](https://docs.openclaw.ai/concepts/memory)  
- **Tradclaw household data (plain markdown in workspace):** `resources/`  
- **Blanks:** `resources/templates/`  

Optional OpenClaw files you can add later if your install uses them: `BOOT.md`, workspace-root `BOOTSTRAP.md` (one-time ritual — different from [`../tradclaw/BOOTSTRAP.md`](../tradclaw/BOOTSTRAP.md) in this repo).
