# memory/

OpenClaw’s memory model is plain markdown in the workspace — see [Memory](https://docs.openclaw.ai/concepts/memory).

## Official pieces (same names OpenClaw uses)

| Piece | Role |
|-------|------|
| **`MEMORY.md`** (workspace root) | Long-term durable facts, preferences, decisions. Tradclaw uses it for household constants; OpenClaw recommends loading it in **main / private** sessions. |
| **`YYYY-MM-DD.md` in this folder** | Daily log — running context. Session start typically includes **today and yesterday**. |
| **`DREAMS.md`** (optional, workspace root) | Experimental dreaming / diary when that feature is enabled — see Memory doc. |

Tools like **`memory_search`** / **`memory_get`** (when the memory plugin is active) operate on these files per OpenClaw docs.

## What goes where in Tradclaw (household convention)

| Use | Where | Examples |
|-----|--------|----------|
| **Short-lived / same-day** | `YYYY-MM-DD.md` here | “Pickup moved to 4,” same-day scratch notes |
| **Stable over months** | `../MEMORY.md` | Allergies, quiet hours, what “urgent” means |
| **Structured records** | `../resources/` | Meal plans, school notices, homework logs |

If it will still matter in a month, prefer `MEMORY.md` or `resources/`. If it is ephemeral, use a dated file here.

## Heartbeats

Gateway [heartbeat](https://docs.openclaw.ai/gateway/heartbeat) runs use **`../HEARTBEAT.md`** (including `HEARTBEAT_OK`). No extra state file is required in `memory/` for that.
