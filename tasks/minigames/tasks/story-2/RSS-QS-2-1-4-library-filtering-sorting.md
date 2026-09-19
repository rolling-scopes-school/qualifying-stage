# Task RSS-QS-2-1-4: Library Games Section Layout (25 points)

## Description

Implement the layout of the Library games section on the Library page according to the Figma mockup.
The section displays static data from the provided mock dataset and includes the page title, filtering controls, and sorting controls.

## Acceptance Criteria

- The section is implemented in full compliance with the project's key layout requirements described in [MiniGames Common Layout Requirements](../../common-layout-requirements.md). This is a mandatory criterion.

**Filtering chips:**

- Clicking a chip makes it active and deactivates the previously selected chip.
- Only one chip can be active at a time.
- Active, inactive, and hover states are styled according to the design style guide.
- No other actions are triggered by clicking a chip at this stage; filtering functionality will be implemented later.

**Sorting control:**

- The currently selected sort method is always reflected in the control.
- Clicking a sort option switches the selection; only one option can be active at a time.
- Active, inactive, and hover states are styled according to the design style guide.
- On selection, the option list closes and the chosen sort method is displayed in the control.
- No other actions are triggered by changing the sort method at this stage; sorting functionality will be implemented later.

Note for students: if the sorting control is implemented with a native `<select>`, keep in mind that on macOS the dropdown behavior can be less flexible for matching the design exactly, so it may be worth considering an alternative approach if pixel-perfect styling is a priority.
