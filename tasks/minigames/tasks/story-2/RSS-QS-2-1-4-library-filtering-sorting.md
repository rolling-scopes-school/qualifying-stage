# Task RSS-QS-2-1-4: Library Games Section Layout (25 points)

## Description

Implement the layout of the Library games section on the Library page according to the Figma mockup.
The section includes the page title, filtering controls, and sorting controls. Category labels and sort options should match the mockup.

## Acceptance Criteria

- The section is implemented in full compliance with the project's key layout requirements described in [MiniGames Common Layout Requirements](../../common-layout-requirements.md). This is a mandatory criterion.
- Using the provided mock data files for category labels or sort option values is optional; hardcoded values taken from the Figma mockup are acceptable at this stage.

**Filtering chips:**

- Clicking a chip makes it active and deactivates the previously selected chip.
- Only one chip can be active at a time.
- Active, inactive, and hover states are styled according to the design style guide.
- When the viewport becomes narrower and the full chip row no longer fits horizontally, chips must not wrap to a new line. Chips that do not fit remain in one row, are clipped by the section boundary, and can be revealed by horizontal swipe/drag within the chips container.
- The chips container may support horizontal overflow scrolling for interaction, but the scrollbar itself must not be visible and must not break the section layout or spacing from the mockup (no extra gap, no shifted controls, no visible scrollbar track/thumb).
- No other actions are triggered by clicking a chip at this stage; filtering functionality will be implemented later.

**Sorting control:**

- The currently selected sort method is always reflected in the control.
- Clicking a sort option switches the selection; only one option can be active at a time.
- Active, inactive, and hover states are styled according to the design style guide.
- On selection, the option list closes and the chosen sort method is displayed in the control.
- No other actions are triggered by changing the sort method at this stage; sorting functionality will be implemented later.

> Note for students: if the sorting control is implemented with a native `<select>`, keep in mind that on macOS the dropdown behavior can be less flexible for matching the design exactly, so it may be worth considering an alternative approach if pixel-perfect styling is a priority.
