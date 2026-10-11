# US 3.3: Chemical Reactions (35 points)

**Level 3 — Full game**

## Goal

Some ingredient combinations create extra effects, so the player must watch more than simple sums.

## What to build

- [ ] This story needs the difficulty selection from **Level 2**.
- [ ] Easy has **no reactions**. Medium enables **2** reactions from the reaction table, and Hard enables **3** reactions from the reaction table.
- [ ] Keep reactions in a typed array like `IReaction[]`, not in one long `if / else` chain.
- [ ] Recalculate cauldron values from the ingredient list every time and apply reactions to these current values.
- [ ] A reaction fires only when it changes from **not active** to **active**. If the same ingredient combination stays active on the next add, it does not fire again until the combination changes.

## Reaction table

| # | Type | Reaction | Trigger | Effect |
|---|---|---|---|---|
| 1 | Ingredients | Bubbling | Fairy Dust + Caustic Acid | Magic Power `+50%`, remove `10` seconds once |
| 2 | Ingredients | Volatile Mix | Phoenix Feather + Essence of the Void | Lose `1` life and clear the cauldron |
| 3 | Ingredients | Solar Frost | Dragon Tears + Frost Lotus | Set Temperature to `0`, increase Density by `20%` |
| 4 | Ingredients | Rooted Steam | Mandrake Root + Toad Slime | Increase Density by `25%`, reduce Magic Power by `10%` |
| 5 | Ingredients | Ashen Bloom | Phoenix Feather + Fairy Dust | Increase Temperature by `10`, increase Magic Power by `25%` |
| 6 | Stats | Annihilation | One ingredient has Temperature `> +15` and another has Temperature `< −15` | Set Temperature to `0` and double Density |
| 7 | Stats | Pressure Spike | Total Density `>= 70` | Set Density to `70` and increase Magic Power by `10%` |
| 8 | Stats | Magma Flux | Total Temperature `>= 60` | Increase Magic Power by `20%` and reduce Density by `10%` |
| 9 | Stats | Deep Freeze | Total Temperature `<= -20` | Increase Density by `15%` and reduce Magic Power by `15%` |
| 10 | Stats | Arcane Saturation | Total Magic Power `>= 80` | Set Magic Power to `80` and increase Temperature by `5` |
| 11 | Mix | Steam Burst | Dragon Tears + Caustic Acid and total Temperature `>= 35` | Increase Temperature by `10` and remove `5` seconds |
| 12 | Mix | Black Ice | Frost Lotus + Essence of the Void and total Density `<= 0` | Reduce Temperature by `10` and increase Magic Power by `20%` |
| 13 | Mix | Heavy Spark | Fairy Dust + Toad Slime and total Density `>= 40` | Increase Density by `20%` and Magic Power by `10%` |
| 14 | Mix | Burning Root | Mandrake Root + Phoenix Feather and total Temperature `>= 40` | Increase Temperature by `15` and reduce Density by `10%` |
| 15 | Mix | Void Resonance | Essence of the Void + Dragon Tears and total Magic Power `>= 50` | Increase Magic Power by `30%` and reduce Temperature by `5` |

## Hints

1. Check `wasActive` on the old ingredient list before you add the new card.
2. Check `isActiveNow` on the new ingredient list after the add.
3. Keep value changes inside each reaction `apply(...)` function.
4. Small code sketch:

```ts
const firedNow = reactions.filter((reaction) => {
  return !reaction.isActive(before) && reaction.isActive(after);
});
```