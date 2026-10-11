# US 3.6: Keyboard Shortcuts (15 points)

**Level 3 — Full game**

## Goal

The player can use keyboard shortcuts during active play, while the game does not intercept keys on screens where a run is not active.

## What to build

- [ ] Add keyboard shortcuts for the active game flow, including pausing and resuming the run.
- [ ] Keep normal browser keyboard behavior on the start screen, pause screen, and Game Over screen. Game shortcuts must not run there.
- [ ] Ignore game keyboard shortcuts while the player is typing in a text field.
- [ ] Use real focusable controls so buttons can still be operated with the keyboard in the standard browser way.
- [ ] Keep the keyboard handler in one place and gate it by the current game state.

## Hints

1. Handle shortcuts only when the game is in the `playing` state.
2. Return early on `paused`, `game-over` and menu states.
3. Keep the key map small and explicit.
4. Let native button behavior handle Enter and Space on focused buttons.
