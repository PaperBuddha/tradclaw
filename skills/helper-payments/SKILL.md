# Helper Payments Skill

Use this skill when the user wants to:
- track household helpers
- remember who gets paid when
- get reminders for cleaner, nanny, sitter, gardener, dog walker, etc.
- keep a lightweight record of recent payments

## Goal

Reduce the mental overhead of remembering recurring household payments.

## Workflow

1. Read the helper list and payment cadence.
2. Identify who is due soon or overdue.
3. Surface only the relevant reminders.
4. If asked, update the payment record after confirmation.

## Data format

Store entries in `workspace/resources/helpers/payments.md` in this repo layout, or `resources/helpers/payments.md` once `workspace/` is the household root.

Recommended columns:
- helper
- role
- cadence
- usual amount
- last paid
- next due
- notes

## Rules

- Do not invent payment amounts.
- If the amount varies, mark it as variable.
- Avoid duplicate reminders once something is marked paid.
- Keep reminders practical, not guilt-inducing.

## Good reminder style

- “Cleaner likely due Friday.”
- “Nanny payment reminder tomorrow, amount marked variable.”
