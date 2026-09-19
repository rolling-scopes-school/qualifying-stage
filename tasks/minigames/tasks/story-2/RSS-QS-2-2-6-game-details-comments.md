# Task RSS-QS-2-2-6: Game Details Dialog — Comments Section Layout (15 points)

## Description

Implement the layout of the Comments section inside the Game Details dialog according to the Figma mockup.
The section contains the section heading, a form for submitting a new comment, and a list of existing comments.

## Acceptance Criteria

- The section is implemented in full compliance with the project's key layout requirements described in [MiniGames Common Layout Requirements](../../common-layout-requirements.md). This is a mandatory criterion.
- The textarea for composing a new comment is implemented according to the design style guide.
- The textarea grows gradually as the user types, up to a maximum height of 88px; once that height is reached, an internal scrollbar appears to allow the user to scroll within the textarea.
- The `Submit` button is styled correctly but does not perform any action at this stage; form submission will be implemented later.
- Clicking a like button toggles it between its active and inactive states; both states are styled according to the design style guide.
- Toggling a like on one comment does not affect the state of like buttons on any other comments.
- No other actions are performed on like click at this stage.
