# US 1.1: Ingredient Shelf & Cauldron (35 points)

**Level 1 — Basic**

## Goal

The player can add ingredients from the shelf to the cauldron. Each ingredient has a limited stock. Level 1 keeps the 3 numbers visible on each card.

## What to build

- [ ] Show **6** ingredient cards from the ordered catalogue in the README.
- [ ] Each card shows the ingredient **name**, a CSS or SVG **icon**, and the 3 numbers directly on the card.
- [ ] Use real `<button>` elements, so click adds the ingredient.
- [ ] At the start of every new game, give each shelf ingredient a random stock: a whole number from **2 to 15**.
- [ ] Show the stock as a number badge on each card.
- [ ] Every add action reduces that ingredient's stock by **1**. The same ingredient can be added several times while its stock is above 0.
- [ ] When the stock is **0**, the slot becomes empty: no icon, dimmed, badge **0**. It stays in place and cannot be clicked or focused.
- [ ] Used ingredients are spent: Brew does not return them and the stock is not refilled.
- [ ] Keep the full **8-item** catalogue in the project, even though Level 1 uses only the first **6** entries.
- [ ] The cauldron keeps the exact order of added ingredients.
- [ ] The cauldron holds at most **4** ingredients.
- [ ] When the cauldron is full, block the shelf and ignore new add actions until the cauldron is cleared. The recipe panel shows the counter `added / maximum` (see US 1.3).

## Hints

1. Start with one `INGREDIENTS` array in the same order as the README table.
2. Make one helper like `addIngredient(id)` that checks the cauldron size before it changes the state.
3. Re-render the shelf and cauldron from `state.cauldronIngredients` after each change.
4. Create the stock with one helper, for example `createStock(ingredients)` that uses `Math.floor(Math.random() * 14) + 2`. Keep it in `state.shelfStock`.
5. Set `disabled` on the button when the stock is 0.
6. Tooltip behavior is not needed yet. It comes in Level 3.
