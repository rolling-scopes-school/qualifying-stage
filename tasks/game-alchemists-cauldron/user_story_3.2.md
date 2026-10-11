# US 3.2: Ingredient Tooltip (15 points)

**Level 3 — Full game**

## Goal

The player can read ingredient numbers in a tooltip instead of on the card.

## What to build

- [ ] In Level 3, shelf cards show only the **icon** and **name**.
- [ ] On hover, show a tooltip with **Temperature**, **Density** and **Magic Power**.
- [ ] Show positive values with `+` and negative values with `−`.
- [ ] If the card is near the right screen edge, open the tooltip to the **left**.
- [ ] If the card is near the bottom edge, open the tooltip **upward**.
- [ ] Keep the tooltip above other game UI.
- [ ] Hide all tooltips while the game is paused.
- [ ] Keyboard and click gameplay from earlier levels must still work.

## Hints

1. Start with one hidden tooltip element inside each card.
2. Add CSS classes like `.tooltip--left` and `.tooltip--up`.
3. If needed, use `getBoundingClientRect()` to choose the side.
4. The tooltip shows only the ingredient base values.