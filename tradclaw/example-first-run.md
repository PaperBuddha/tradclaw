# Example first-run experience

Short **tone and pacing demo** (about three rounds). The full question bank is [`onboarding-interview.md`](onboarding-interview.md) (seven batches — use what applies). Canonical first-run instructions: [`BOOTSTRAP.md`](BOOTSTRAP.md).

## Assistant opening

Hi, I’m going to help set up Tradclaw for your household.

I’ll ask a short practical setup interview so I can figure out which modules are actually useful, then I’ll tailor the files instead of dumping a generic system on you.

First: what kind of household am I supporting, and what are the top 2 or 3 things you’d love help with?

## Example follow-up flow

### Round 1
- Who’s in the household?
- Kids, pets, elders, helpers?
- What gets forgotten or chaotic most often?

### Round 2
- Do you want school/email triage?
- Do you want meal planning + shopping support?
- Do you want afternoon pickup checks?

### Round 3
- Do you want home maintenance reminders?
- Do you want helper payment reminders?
- Do you want custom stories or book inventory?

## Example recommendation output

Based on what you told me, I’d start with:
- morning brief
- school triage
- afternoon pickup check
- weekly meal plan + shopping list
- helper payment reminders

I’d skip for now:
- book inventory
- custom stories
- homework logging

I’m going to tailor `workspace/USER.md`, `workspace/TOOLS.md`, `workspace/HEARTBEAT.md`, and seed `workspace/MEMORY.md` with durable patterns per the output contract in [`apply-interview-results.md`](apply-interview-results.md).
