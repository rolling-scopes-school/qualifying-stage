# Task RSS-QS-1-4-4: Carousel Section Layout (25 points)

## Description

Implement the static layout of the carousel/slider section on the Home page according to the Figma mockup.  
At this stage only the visual layout is required; carousel interactivity and slide switching will be implemented in a separate task.

## Acceptance Criteria

- The section is implemented in full compliance with the project's key layout requirements described in [MiniGames Common Layout Requirements](../../common-layout-requirements.md). This is a mandatory criterion.
- **Card Width Thresholds (per latest Figma mockup):** Static slider card layout should already encode the responsive 288px information-display rule:
  - Cards rendered at **288px width or wider** display a bottom info overlay containing (at minimum, per mockup): **game title**, **likes count**, and **rating stars** (or numeric rating). Title text is single-line and truncated with an ellipsis (`…`) if it overflows the allocated width.
  - Cards rendered at **width smaller than 288px** display **only the game image** — no text, no rating, no icons, no info overlay.
- Navigation arrows and indicators are non-functional at this stage (interactivity will be added later).
