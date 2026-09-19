# Task RSS-QS-2-3-1: Home Page Slider Logic (80 points)

## Description

Implement the interaction logic of the Home page slider according to the Figma mockup.
The static layout of the slider was implemented in Story 1; this task covers slider behavior, card state transitions, and autoplay logic.

## Scope

At this stage, **only the slider logic is evaluated**. Pixel-perfect accuracy is not checked. The slider should visually match the mockup at all breakpoints — correct card counts, proportions, and overall appearance — but exact pixel measurements are not required.

## Acceptance Criteria

- The slider preserves the layout requirements and card composition defined by the mockup at all project breakpoints.
- At each breakpoint, the carousel displays the number of cards and card sizes defined in the mockup.
- **Card Width Thresholds:**
  - **Cards with rendered width of 288px or larger** display full information overlay on the bottom gradient: game **title**, **likes**, and **rating stars** (all three elements per mockup).
  - **Cards with rendered width smaller than 288px** display **only the image** (no title, no rating, no likes text, no info overlay — the card is purely visual).
- **Title Text Truncation on Slider Cards:** If the game title on an info-enabled slider card (≥288px) does not fit into the allocated single-line space, it should be truncated with a trailing ellipsis (`…`) via CSS.
- **Card Click Opens Game Details Dialog:** Clicking on any slider card (regardless of its current displayed size) triggers the same Game Details dialog as clicking a game card from the Library page. The dialog should be opened with the data corresponding to the clicked slider card.
- Slider movement is available in both directions.
- The slider can be moved by swipe gesture.
- The slider can be moved by arrow buttons.
- The slider automatically advances one step from right to left every 4 seconds.
- During sliding, card sizes change smoothly and are animated.
- Cards grow larger as they move closer to the center.
- Cards become smaller as they move farther from the center.
- If the user presses and holds the carousel, the autoplay timer is paused and no automatic transition occurs while the interaction is active.
- If the user releases the carousel without making a swipe, the timer resumes and the next automatic slide occurs when the remaining timer duration finishes.
- If the user performs a manual swipe after pressing and holding, the autoplay timer resets and a new 4-second countdown starts.
- The slider is implemented using TypeScript and SCSS only. Third-party slider/carousel libraries are not allowed.

## Notes

> **Reference:** [Material Design 3 — Carousel guidelines](https://m3.material.io/components/carousel/guidelines) — for design inspiration and interaction patterns only. Implementation should follow the project's Figma mockup.
