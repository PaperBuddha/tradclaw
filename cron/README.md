# Cron jobs (optional)

This folder contains **example** scheduled jobs for Tradclaw. They are **not** core to the scaffold.

**Do not copy this folder or `jobs.template.json` literally into a live OpenClaw config.** Treat it as a sketch of what a job *could* look like: the `id` strings, cron expressions, `timezone` fields, and clock times are placeholders for Pacific-time-style demos. In real use, invent your own IDs, match your timezone, and pick schedules that fit your household.

## When to use this folder

Pick cron jobs **after** household setup and module selection (see [`../tradclaw/BOOTSTRAP.md`](../tradclaw/BOOTSTRAP.md) and [`../tradclaw/module-selection-guide.md`](../tradclaw/module-selection-guide.md)). Prompts should assume the household template lives under [`../workspace/`](../workspace/) until the user copies it elsewhere.

## File

- `jobs.template.json` — sample job **shapes** (goals + prompts). Adapt fields; do not assume repo IDs or timestamps are correct for your install (all entries default to `enabled: false`)

## Plain-language job ideas (adapt timing to your life)

Use these as **what to schedule**, not as copy-paste config. Match cadence to your timezone and OpenClaw cron format.

| Idea | Typical timing (example) | Task in plain language |
|------|--------------------------|-------------------------|
| Morning brief | Weekdays, before the rush | Calendar, school inboxes, weather if useful, helper day — actionable summary only; optional one fun fact if the household wants it |
| Afternoon pickup | Weekdays, ~60–90 min before pickup | Same-day calendar + school messages; gear, forms, snacks, uniforms |
| Weekend preview | Friday evening | Sat/Sun activities, sports times, prep and conflicts |
| Meal plan | Sunday afternoon | Week of dinners from calendar load; grocery gaps |
| School deadline sweep | Midweek | Forms, fees, spirit days, trips — skip newsletter noise |
| Helper payment | Matches pay cadence | Who is due; amount only if stored confidently |
| Home maintenance | Monthly-ish | 2–4 realistic tasks from your schedule file |
| Homework review | Weekly | Patterns from homework logs; reinforce concepts |
| Storytime | Optional evenings | Optional story prompt if household uses story mode |

## How to use it

Do not enable everything.

Pick only the jobs that match the household’s actual needs.
A small number of good scheduled checks beats a giant automation hairball.

## Good starter picks (concepts, not copy-paste IDs)

These names match example entries in `jobs.template.json` so you can find the right **idea**. Rename and reschedule when you implement:

- morning brief  
- afternoon pickup check  
- weekend preview  
- meal plan prompt  

Add later if useful:

- school deadline sweep  
- helper payment reminder  
- monthly home maintenance  
- homework review  
- storytime prompt  

## Advice

- Use cron for exact timing.
- Use heartbeat for lighter rotating checks (see `workspace/HEARTBEAT.md`).
- Keep messages short and actionable.
- If a job creates too much noise, disable it or reduce frequency.
