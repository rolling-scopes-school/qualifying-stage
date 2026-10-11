# US 2.1: Difficulty Selection (25 points)

**Level 2 — Extended**

## Goal

The player can choose Easy, Medium or Hard before the game starts.

## What to build

- [ ] Show a **Help** button on the start screen that opens the game rules.
- [ ] The start screen shows an empty shelf and an empty cauldron, score and time at `0`, no life icons, and a centered **Start Game** button.
- [ ] Show a **Settings** or **Menu** button on the start screen that opens the difficulty panel.
- [ ] Inside the Settings/Menu panel, show **Easy**, **Medium** and **Hard** buttons.
- [ ] Use all values from the README difficulty table for the chosen difficulty.
- [ ] **Medium** must match the full Level 1 rule set.
- [ ] **Medium** and **Hard** start with **150 seconds** and **3 lives**.
- [ ] The chosen difficulty sets shelf size, cauldron limit, start time, tolerance, lives, score per brew, time bonus and reaction count.
- [ ] The player cannot change difficulty during a running game.
- [ ] Save the chosen difficulty in the game state.
- [ ] The leaderboard becomes one Top-10 list per difficulty and shows a **Difficulty** column.
- [ ] The random recipe picker must use the recipe rows for the chosen difficulty: **Easy / Medium / Hard** from the README recipe table.
- [ ] At the start of the game, show only the ingredients needed for the chosen difficulty on the shelf, and give those ingredients random stock (2–15).

## Hints

1. Keep one `DIFFICULTY_SETTINGS` object keyed by difficulty.
2. Build the short button text from the same settings object.
3. Create the first game state from the clicked difficulty button.
4. Reuse the same leaderboard UI and change only the stored list key and the extra column.
