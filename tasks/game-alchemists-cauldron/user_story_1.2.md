# US 1.2: Cauldron Parameter Bars (25 points)

**Level 1 — Basic**

## Goal

The player sees the cauldron values change right after every added ingredient.

## What to build

- [ ] Show 3 bars: **Temperature**, **Density** and **Magic Power**.
- [ ] An empty cauldron starts at **0 / 0 / 0**.
- [ ] The current values are the sum of the added ingredient values.
- [ ] Support negative values. For bars with negative values, the center line means **0**.
- [ ] Animate each bar change smoothly when the value changes.
- [ ] Show the current recipe target zone on every bar.
- [ ] Show a marker for the current value on every bar.
- [ ] Add a green glow when the current value is inside the recipe range.

## Hints

1. Write one pure function like `calculateCauldron(ingredients)`.
2. Keep recipe data and current cauldron values as separate objects.
3. Use CSS transitions for smooth movement.
4. Render all 3 bars from the same helper so they stay consistent.
