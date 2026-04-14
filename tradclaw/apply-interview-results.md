# Applying Interview Results

After the onboarding interview, the assistant should not just say “great.”
It should actively shape the workspace.

In the Tradclaw repository, household files live under **`workspace/`**. After the user copies this tree into their OpenClaw home, the same filenames usually sit at the **workspace root** — adjust paths if their layout differs.

## Output contract

After the interview, produce:
1. a short summary of what was learned
2. the recommended enabled modules
3. the recommended disabled modules
4. the file changes to make
5. optional cron suggestions

**Recommended:** show items 1–5 to the user and confirm before editing `workspace/` files, unless they asked you to proceed immediately.

## Files to tailor

Paths below are under `workspace/` in this repo (template root once deployed).

### `IDENTITY.md`
Keep aligned with OpenClaw: short **name and emoji** line. Extended persona stays in `SOUL.md`.

### `USER.md`
Add:
- household structure
- high priority pain points
- preferred briefing times
- quiet hours
- story preferences if relevant

### `TOOLS.md`
Add:
- calendars to watch
- school channels
- helpers and payment cadence
- grocery / shopping tools
- maintenance notes

### `HEARTBEAT.md`
Tailor to the household’s real needs.
Good examples:
- school triage on weekdays only
- afternoon pickup check only on activity days
- meal pulse every other day instead of daily

### `MEMORY.md`
Seed only the durable patterns:
- recurring family rhythms
- what counts as urgent
- recurring tasks worth remembering

## Module recommendation format

Example:
- Enable now:
  - calendar briefs
  - school triage
  - meal planning and shopping
  - helper payments
- Leave off for now:
  - book inventory
  - custom stories

## Good assistant behavior

Good:
- “You seem to need school triage and afternoon pickup checks more than weekly home maintenance.”
- “You don’t sound interested in bedtime stories, so I’d leave that module off for now.”

Bad:
- enabling everything by default
- forcing a huge system on a household with only one or two pain points
