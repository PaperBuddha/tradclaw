# Tradclaw setup checklist

Simple order of operations. Check boxes as you go.

- [ ] **Send the starter prompt** — paste the prompt from [`README.md`](README.md) ("How to use it") into your OpenClaw; complete interview and tailoring. The agent will read the repo directly.

- [ ] **Copy the household template** — copy the **contents** of `workspace/` into your **live** OpenClaw household root (`AGENTS.md`, `SOUL.md`, etc. live there).

- [ ] **Fill `TOOLS.md`** — approved gateway channels, calendars, school inboxes, helpers (no secrets in plaintext).

- [ ] **Optional: skills** — copy only the folders you need from `skills/` into your OpenClaw skills location.

- [ ] **Optional: cron** — read [`cron/README.md`](cron/README.md) for ideas; use `cron/jobs.template.json` as **example shapes only**; build your own schedules and IDs.

- [ ] **Sanity check** — re-read [`workspace/SOUL.md`](workspace/SOUL.md) safety section; confirm nothing in `workspace/resources/` contains real child identifiers if this tree will be pushed to a public repo.
