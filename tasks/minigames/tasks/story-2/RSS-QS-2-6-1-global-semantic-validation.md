# Task RSS-QS-2-6-1: Global Layout Verification (12 points)

## Description

This task defines global layout checks that apply to the whole Story 2 implementation.
The layout should be valid and semantic.

## Acceptance Criteria

- The layout is valid, semantic, and matches the design.
- HTML validation covers all required states listed below.

## HTML Validation Rules

- Use <https://validator.w3.org/> to validate markup.
- Full points for a checked state are awarded when the validator shows:
  - `Document checking completed. No errors or warnings to show.`
- If there are warnings but no errors, award half points for the checked state.
- Validator **info** messages are not treated as errors or warnings and should be ignored during scoring.

## How to Validate When SPA Is Used

[Story 2](../../story-2.md) introduces a second page and a new dialog. Validate the following states separately:

1. **Library page (default state):** open the Library page in the browser, right-click and choose **View Page Source**, copy the full source, paste into <https://validator.w3.org/> using **Validate by Direct Input**, and run validation.
2. **Game Details dialog open:** open the Game Details dialog on the Library page, then repeat the View Page Source → validator steps.
3. **Mobile menu open** (≤ 768px): open the burger menu at a mobile viewport on the Library page, then repeat the View Page Source → validator steps.
