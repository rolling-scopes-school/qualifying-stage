# US 3.1: Drag & Drop (20 points)

**Level 3 — Full game**

## Goal

The player can drag an ingredient card into the cauldron with the mouse.

## What to build

- [ ] Add mouse drag from a shelf card into the cauldron with HTML5 drag events.
- [ ] Use `dragstart`, `dragover`, `dragleave` and `drop`.
- [ ] Highlight the cauldron as a drop zone while a valid drag is over it.
- [ ] Keep click add actions working.
- [ ] Level 3 starts with **150 seconds** and **3 lives**.
- [ ] Ignore drop actions when the game is paused.
- [ ] Ignore drop actions when the cauldron is already full.
- [ ] Do not allow dragging an ingredient whose stock is 0. A successful drop reduces the stock by **1**, like a click.
- [ ] After a successful drop, add the same ingredient as the click action would add.
- [ ] Touch dragging is optional.

## Hints

1. Start with the click flow, then reuse that logic in `handleDrop`.
2. Put the ingredient `id` into `dataTransfer`.
3. Toggle one CSS class for the highlighted cauldron.
4. Remove the highlight in both `drop` and `dragleave`.
