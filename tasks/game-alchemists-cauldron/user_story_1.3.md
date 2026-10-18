# US 1.3: Recipe & Brewing Check (45 points)

**Level 1 — Basic**

## Goal

The player gets one random recipe from the README recipe table, mixes ingredients and checks the result with the **Brew** button.

## What to build

- [ ] Show a recipe panel with a fantasy name and 3 target ranges from the recipe table in the README.
- [ ] Show an ingredient counter on the recipe panel, for example **Ingredients: 2 / 4** (added / maximum). The maximum is the cauldron capacity from the difficulty table (**4** in Level 1).
- [ ] Update the counter every time the cauldron content changes: an ingredient is added, after Brew, and after a restore from a save.
- [ ] When the counter reaches the maximum (**4 / 4**), highlight it, so the player understands why the shelf is blocked.
- [ ] Keep a fixed array of **20** recipes from the README table.
- [ ] At the start of a new game and after every successful brew, choose **one random recipe** from that table.
- [ ] Pick recipes by difficulty only: Easy uses Easy recipes, Medium uses Medium recipes, Hard uses Hard recipes.
- [ ] The **Brew** button is hidden or disabled on the start screen; before the first run, show **Start Game** in the center instead.
- [ ] Level 1 has **no reactions**. The recipe data and the brew check use only the ingredient sums.
- [ ] Enable **Brew** only when the cauldron has at least **1** ingredient.
- [ ] On brew, calculate the current **Temperature**, **Density** and **Magic Power**, then check each parameter against the recipe range expanded by the Level 1 tolerance **±8**.
- [ ] On success, add **200** score, add **10 s** up to **150 s**, clear the cauldron and generate a new recipe. On failure, lose **1** life and clear the cauldron.

## Hints

1. Put the 20 recipe rows from the README into one `RECIPES` array in `recipes.ts`.
2. Write one helper like `getRecipesByDifficulty(difficulty)`.
3. The counter text is simply `` `Ingredients: ${cauldronIngredients.length} / ${settings.maxCauldronIngredients}` ``.
4. Worked example: recipe **32..42**, tolerance **±8**, checked range **24..50**. A current value of **37** passes.
5. Small code sketch:

```ts
const availableRecipes = RECIPES.filter(
  (recipe) => recipe.difficulty === "medium",
);

const activeRecipe = pickRandom(availableRecipes);
```
