# US 3.4: Pour Out (10 points)

**Level 3 — Full game**

## Goal

The player can clear a wrong mixture without losing a life.

## What to build

- [ ] Show a **Pour Out** button during play.
- [ ] Clicking it clears the whole cauldron.
- [ ] **Pour Out** costs **10 seconds**.
- [ ] The player does **not** lose a life.
- [ ] Disable the button when the cauldron is empty.
- [ ] The ingredients that were in the cauldron are **not** returned to the shelf.
- [ ] Keep all other game state values unchanged.

## Hints

1. This action is needed because a wrong mixture should not force the player to click **Brew**.
2. Reuse the same cauldron-clear helper used after brew results.
3. Check the empty state before you subtract time.
