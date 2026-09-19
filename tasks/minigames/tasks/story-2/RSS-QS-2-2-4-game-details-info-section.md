# Task RSS-QS-2-2-4: Game Details Dialog — Game Info Section Layout (15 points)

## Description

Implement the layout of the game info section inside the Game Details dialog according to the Figma mockup.
The section contains the game title, description, characteristic badges, and action buttons (Play Now, Add to Favorites).

## Acceptance Criteria

- The section is implemented in full compliance with the project's key layout requirements described in [MiniGames Common Layout Requirements](../../common-layout-requirements.md). This is a mandatory criterion.
- On desktop and tablet breakpoints the dialog is displayed at a width of 600px; on mobile (375px) the dialog takes the full 375px width.
- The title, description, and characteristic badges are displayed according to the mockup.
- The primary action button and `Add to Favorites` button are present and styled correctly, including hover and active states.
- **Primary Action Button Logic (per game pricing type):**
  - For **free** games, the primary action button displays `Play Now` text as per the mockup.
  - For **paid** games, the primary action button displays `Buy Now: $<price>` text (e.g. `Buy Now: $4.99`), where the price value is taken from the game data. Paid button styling follows the Figma mockup (same size as Play Now).
- Clicking the primary action button (`Play Now` or `Buy Now`) does not perform any action.
- Clicking `Add to Favorites` toggles the button between its active and inactive states. Both states are styled according to the design style guide.
