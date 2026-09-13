# Task RSS-QS-1-6-1: Global Layout Verification (16 points)

## Description

This task defines global layout checks that apply to the whole Story 1 implementation.
The layout should be valid and semantic.

## Acceptance Criteria

- The layout is valid, semantic, and matches the design.
- HTML validation for both pages: Home plus Auth.

## HTML Validation Rules

- Use <https://validator.w3.org/> to validate markup.
- Full points for a checked page are awarded when the validator shows:
  - `Document checking completed. No errors or warnings to show.`
- If there are warnings but no errors, award half points for the checked page.
- Validator **info** messages are not treated as errors or warnings and should be ignored during scoring.

## How to Validate When SPA Is Used

Since [Story 1](../../story-1.md) has a single page, validate the following states separately:

1. **Home page (default state):** open the deployed page in the browser, right-click and choose **View Page Source**, copy the full source, paste into <https://validator.w3.org/> using **Validate by Direct Input**, and run validation.
2. **Auth dialog open:** open the Auth dialog on the Home page, then repeat the View Page Source → validator steps.
3. **Mobile menu open** (≤ 768px): open the burger menu in the browser at a mobile viewport, then repeat the View Page Source → validator steps.
