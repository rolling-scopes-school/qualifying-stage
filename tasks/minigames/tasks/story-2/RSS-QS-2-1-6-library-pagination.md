# Task RSS-QS-2-1-6: Pagination Section Layout (15 points)

## Description

Implement the layout of the pagination section on the Library page according to the Figma mockup.

## Acceptance Criteria

- The section is implemented in full compliance with the project's key layout requirements described in [MiniGames Common Layout Requirements](../../common-layout-requirements.md). This is a mandatory criterion.
- Page number buttons and arrow buttons are present and styled according to the design style guide, including default, hover, active, and disabled states.
- Clicking a page number button makes that page active; only one page can be active at a time.
- Clicking a page number button updates the visual state of all pagination controls accordingly.
- When the first page is active, the previous arrow button is disabled.
- When the last page is active, the next arrow button is disabled.
- Clicking the previous or next arrow button switches to the adjacent page, unless the corresponding arrow is disabled.
- **Visible Page Button Limit (per Figma mockup):**
  - On **desktop and tablet** breakpoints, the pagination control displays at most **4 page number buttons** at a time (plus navigation arrows). If the total number of pages exceeds 4, only 4 buttons are shown (e.g. pages 2–5 when page 3 is active).
  - On **mobile** breakpoints, the pagination control displays at most **3 page number buttons** at a time (plus navigation arrows).
  - If the actual total number of pages is less than the per-breakpoint maximum (e.g. only 2 pages total), exactly that number of buttons is rendered (no placeholder or ghost buttons for non-existent pages).
- No actual content updates occur at this stage; only the pagination control state changes.
