# US 2.2: Auto-save & Continue Game (25 points)

**Level 2 — Extended**

## Goal

If the page reloads or closes, the player can continue the unfinished game.

## What to build

- [ ] Save these fields: `difficulty`, `score`, `timeLeft`, `lives`, `activeRecipe`, `cauldronIngredients`, `shelfStock` and `status`.
- [ ] Save after every change that matters and also on pause.
- [ ] On page load, show **Continue Game** only when a valid unfinished save exists.
- [ ] **Continue Game** restores the saved state and opens the game in **paused** state. The saved stock is restored, it is not re-rolled.
- [ ] Finished games are never offered as continue.
- [ ] Starting a new game overwrites the old unfinished save.
- [ ] **Exit to Menu** clears the save.
- [ ] Broken or missing saved data must never crash the game. Use `try/catch` and validation.

## Hints

1. Keep 3 helpers: `saveGame`, `loadGame` and `clearSave`.
2. Save `timeLeft`, not a running interval id.
3. Write one validator like `isValidSave(data: unknown)` before you use loaded data.
4. If the save is broken, delete it and start normally.
