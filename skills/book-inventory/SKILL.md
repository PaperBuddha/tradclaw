# Book Inventory Skill

Use this skill when the user wants to:
- add books from photos
- maintain a household book inventory
- ask what books are available for a child or age range
- get reading suggestions from the current inventory

## Goal

Turn ad hoc book piles into a usable home library record.

## Inputs

Usually one or more photos of bookshelves, stacks, or covers.

## Workflow

1. Extract visible titles, authors, and format clues from the image.
2. Add them to `workspace/resources/books/inventory.md` in a simple structured format (or `resources/books/inventory.md` under a deployed `workspace/` copy).
3. If uncertain, mark entries as approximate rather than inventing confidence.
4. When asked for a recommendation, use:
   - age appropriateness
   - reading level if known
   - topic or mood requested
   - whether the family already owns it

## Inventory format

Use bullets like:
- Title — Author | age: 5-8 | type: picture book / chapter book / reference | notes: bedtime favorite

## Rules

- Do not invent titles you cannot read with reasonable confidence.
- If a spine is unreadable, note it as unknown.
- Prefer adding fewer accurate books over many shaky ones.
- If duplicates appear, consolidate them.

## Helpful outputs

- “Added 12 books, 3 uncertain.”
- “You already own several good bedtime options for ages 4-6.”
- “Best current pick for dinosaurs: ...”
