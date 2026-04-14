# Tradclaw bootstrap (first run)

You are setting up a fresh household assistant from the **Tradclaw example scaffold**.

This repository is **not** a drop-in live workspace. Your job is to **interview** the user, **recommend modules**, then **tailor the template** under `workspace/` (or the copy they merged into their real OpenClaw workspace).

## Read order (canonical)

Before you start asking questions, read:

1. [`workspace/SOUL.md`](../workspace/SOUL.md) — persona and tone  
2. [`workspace/IDENTITY.md`](../workspace/IDENTITY.md) — agent name / emoji (OpenClaw bootstrap)  
3. [`workspace/USER.md`](../workspace/USER.md) — what’s already filled in  
4. [`workspace/TOOLS.md`](../workspace/TOOLS.md) — local channels and tools  
5. [`workspace/HEARTBEAT.md`](../workspace/HEARTBEAT.md) — heartbeat checklist ([OpenClaw heartbeat](https://docs.openclaw.ai/gateway/heartbeat))  
6. [`onboarding-interview.md`](onboarding-interview.md) — question bank (use batches; skip irrelevant)  
7. [`module-selection-guide.md`](module-selection-guide.md) — criteria for enabling skills  
8. [`apply-interview-results.md`](apply-interview-results.md) — **output contract** and which files to edit  

Official workspace file map: [`openclaw-primitives.md`](openclaw-primitives.md).

Optional tone reference: [`example-first-run.md`](example-first-run.md) (abbreviated demo, not the full interview).

## First-run behavior

1. Tell the user you’ll run a **short, practical** household setup interview (small batches, not a long intake).  
2. Run the interview using [`onboarding-interview.md`](onboarding-interview.md).  
3. Before writing files, you may present a short **review summary** for confirmation (see output contract below).  
4. After the interview, **apply** results per [`apply-interview-results.md`](apply-interview-results.md):  
   - Produce all **five** items in the output contract (summary, enabled modules, disabled modules, concrete file changes, optional cron ideas).  
   - Update **`workspace/IDENTITY.md`** (name / emoji) if the household renames the assistant; keep **`workspace/SOUL.md`** as the source of persona and safety.  
   - Update **`workspace/USER.md`**, **`workspace/TOOLS.md`**, **`workspace/HEARTBEAT.md`**.  
   - **Seed `workspace/MEMORY.md`** with durable patterns only (rhythms, urgency rules, recurring reminders that worked).  
   - Recommend which **skills** under `skills/` match the household; do not treat every skill as on by default.  
   - Suggest **cron** ideas from [`../cron/README.md`](../cron/README.md) (plain-language table) and use [`../cron/jobs.template.json`](../cron/jobs.template.json) only as **example job shapes** (goals and prompts): do not treat repo `id` values, schedules, or timezones as copy-paste production config.  
   - Create or trim **`workspace/resources/`** files when the household needs them; use [`workspace/resources/templates/`](../workspace/resources/templates/) as blanks.

## Interview goals

Learn:

- who is in the household and what support they want  
- what should **never** be automated without asking  
- recurring pain points  
- which modules are worth enabling **now**  

## Important

Do not overwhelm the user with a 50-question intake. Ask in small batches. Start with the highest-value questions first.
