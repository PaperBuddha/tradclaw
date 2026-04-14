# OpenClaw primitives (official)

Tradclaw should stay aligned with how OpenClaw actually works. This page summarizes **documented** workspace behavior so the template does not invent parallel concepts.

Primary sources (read these if anything here drifts):

- [Agent workspace](https://docs.openclaw.ai/concepts/agent-workspace) — workspace directory, default path, what each file means  
- [Agent Runtime](https://docs.openclaw.ai/concepts/agent) — bootstrap files injected each session, skills load order  
- [Memory](https://docs.openclaw.ai/concepts/memory) — `MEMORY.md`, daily logs, optional dreaming / `DREAMS.md`  
- [Heartbeat (Gateway)](https://docs.openclaw.ai/gateway/heartbeat) — scheduled main-session turns, `HEARTBEAT.md`, `HEARTBEAT_OK`  
- [Default AGENTS.md](https://docs.openclaw.ai/reference/AGENTS.default) — session-start read order and safety defaults  

## Workspace (required concept)

OpenClaw uses **one workspace directory** (`agents.defaults.workspace`, commonly `~/.openclaw/workspace`) as the agent’s **cwd** for file tools and context. It is separate from `~/.openclaw/` (config, credentials, sessions). See [Agent workspace](https://docs.openclaw.ai/concepts/agent-workspace).

## Bootstrap files (injected at session start)

OpenClaw expects these **in the workspace** (names matter):

| File | Role |
|------|------|
| `AGENTS.md` | Operating instructions, priorities, how to use memory — loaded every session |
| `SOUL.md` | Persona, tone, boundaries — loaded every session |
| `USER.md` | Who the user is, how to address them — loaded every session |
| `IDENTITY.md` | Agent name, vibe, emoji — often filled during onboard |
| `TOOLS.md` | **Guidance only** for local tools and conventions; does **not** control which tools exist |
| `HEARTBEAT.md` | Optional **short** checklist for [heartbeat](https://docs.openclaw.ai/gateway/heartbeat) runs |
| `BOOT.md` | Optional startup checklist when internal hooks are enabled |
| `BOOTSTRAP.md` | **One-time** first-run ritual in the **live** workspace; delete after completion (OpenClaw may recreate only for brand-new workspaces) |
| `memory/YYYY-MM-DD.md` | Daily memory log — today + yesterday recommended on session start |
| `MEMORY.md` | Optional curated long-term memory — prefer loading in **main / private** sessions only |
| `skills/` (optional) | Workspace-specific skills — **highest precedence** for that workspace when names collide |
| `canvas/` (optional) | Canvas UI files |

Missing files get a marker in context; `openclaw setup` can seed defaults. Large files may be truncated per config — see workspace doc.

## Memory (official model)

Per [Memory](https://docs.openclaw.ai/concepts/memory):

- **`memory/YYYY-MM-DD.md`** — running context and observations (one file per calendar day).  
- **`MEMORY.md`** — durable facts, preferences, decisions.  
- **`DREAMS.md`** (optional, experimental) — dreaming / diary surfaces when that feature is enabled.

Recall can use **`memory_search`** / **`memory_get`** from the active memory plugin (defaults described in the Memory doc).

The [Default AGENTS.md](https://docs.openclaw.ai/reference/AGENTS.default) doc also mentions a legacy root **`memory.md`** (lowercase) when `MEMORY.md` is absent; prefer **`MEMORY.md`** only and avoid keeping both on purpose.

## Heartbeat (official)

Per [Heartbeat](https://docs.openclaw.ai/gateway/heartbeat):

- A **scheduled main-session turn** (not the same thing as detached [cron / background tasks](https://docs.openclaw.ai/automation)).  
- Default behavior references **`HEARTBEAT.md`** when present.  
- **`HEARTBEAT_OK`** is the standard ack when nothing needs attention (see doc for stripping rules).

## Skills (load precedence)

Highest precedence first (from [Agent Runtime](https://docs.openclaw.ai/concepts/agent)):

1. Workspace `skills/`  
2. Project agent `/.agents/skills`  
3. Personal `~/.agents/skills`  
4. Managed `~/.openclaw/skills`  
5. Bundled skills  
6. `skills.load.extraDirs`  

Tradclaw ships example skills at **repo** `skills/` for copying into workspace or managed dirs as you prefer.

## Tradclaw-only additions (not named in the workspace file map)

These are **valid plain files** in the workspace (OpenClaw still uses the directory as cwd); they are **household domain** layout, not separate OpenClaw “primitives”:

- **`resources/`** — structured markdown for meals, school, homework, etc.  
- **`tradclaw/`** at **repository** root — interview + module docs for this **scaffold**; usually **not** copied into `~/.openclaw/workspace` unless you want it there.

### `tradclaw/BOOTSTRAP.md` vs OpenClaw `BOOTSTRAP.md`

- **OpenClaw** `BOOTSTRAP.md` lives **in the live workspace**, is a **one-time ritual**, and is meant to be **removed** after completion.  
- **Tradclaw** [`BOOTSTRAP.md`](BOOTSTRAP.md) in this folder is the **example household** setup runbook while you are still inside this git repo. When you copy `workspace/` into your real OpenClaw workspace, OpenClaw may still create or expect its own workspace `BOOTSTRAP.md` for a brand-new install — follow OpenClaw’s onboard flow and do not assume the two files are interchangeable without reading both.
