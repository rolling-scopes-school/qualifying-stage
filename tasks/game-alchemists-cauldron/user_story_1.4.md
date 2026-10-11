# US 1.4: Timer & Game Over (30 points)

**Level 1 — Basic**

## Goal

The player sees the time and lives during play, and the game ends with a clear final screen.

## What to build

- [ ] Show the remaining time as **MM:SS** and as a bar that gets smaller.
- [ ] Level 1 starts with **150 seconds** and **3 lives**.
- [ ] Calculate time from timestamps, not by counting ticks, so the timer stays correct after a background tab.
- [ ] When less than **15 seconds** remain, make the timer red and pulsing.
- [ ] After a successful brew, add the normal time bonus, but never go above the start time.
- [ ] Show the current lives during play.
- [ ] End the game at `00:00`, when lives reach **0**, or when the ingredients run out (see **Out of ingredients** in the README). Show the reason on the Game Over screen.
- [ ] Show a **Game Over** screen with the final score and a **Play again** button.

## Hints

1. Store `endTime = Date.now() + timeLeft` while the game is running.
2. Recalculate `timeLeft` from `endTime - Date.now()` every update.
3. Use one formatter like `formatTime(timeLeft)` for the label.
4. Keep the game-over screen separate from the main game field.