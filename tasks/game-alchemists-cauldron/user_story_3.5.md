# US 3.5: Visual Feedback (20 points)

**Level 3 — Full game**

## Goal

The game gives clear visual feedback for success, failure and active ingredients.

## What to build

- [ ] Add a success animation when a brew is correct.
- [ ] Add an explosion animation and a short screen shake when a brew fails.
- [ ] Make ingredient icons float inside the cauldron.
- [ ] Keep the parameter bars smooth while values change.
- [ ] The green target-zone glow is already part of Level 1. Do not count it again here.
- [ ] A floating `+10s` text after a success is optional.
- [ ] Use CSS animations only for visual effects.
- [ ] Do not use `setInterval` or `setTimeout` for visual animation work.

## Hints

1. Add and remove CSS classes for success and failure states.
2. Keep the animation timing in CSS, not in game logic.
3. Reuse the ingredient data to render floating icons inside the cauldron.
4. Test the animations after both success and failure flows.
