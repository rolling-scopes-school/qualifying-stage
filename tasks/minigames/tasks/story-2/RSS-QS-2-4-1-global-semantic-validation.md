# Task RSS-QS-2-4-1: Global Layout Verification (12 points)

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

[Story 2](../../story-2.md) introduces a second page and a new dialog. Because the application is an SPA, do **not** use **View Page Source** for scoring: it reflects the initial static HTML shell, not the rendered DOM. Validate the markup of the rendered document instead.

For each required state:

1. Open the target state in the browser.
2. Open DevTools → **Elements**.
3. Copy the rendered root markup (for example, the `html` element via Copy → Copy outerHTML).
4. Paste it into <https://validator.w3.org/> using **Validate by Direct Input** and run validation.

Validate the following states separately:

1. **Library page (default state):** open the Library page and validate the rendered markup.
2. **Game Details dialog open:** open the Game Details dialog on the Library page and validate the rendered markup.
3. **Mobile menu open** (≤ 768px): open the burger menu at a mobile viewport on the Library page and validate the rendered markup.
