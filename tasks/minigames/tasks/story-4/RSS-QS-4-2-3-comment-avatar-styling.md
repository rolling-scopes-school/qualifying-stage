# Task RSS-QS-4-2-3: Comment Avatar Styling (3 points)

## Description

Style commenter avatars with random design token background colors and commenter username initials.

## Acceptance Criteria

- **Random Token Color:** Avatar background color is selected randomly from the set of `avatar-random` design tokens.
- **Stable Color Assignment:** Keep the selected color stable for the commenter while the comments view is mounted; ordinary re-renders must not randomly change avatar colors.
- **Username Initial:** The character inside the avatar displays the first non-whitespace character of the commenter's username in uppercase (`.trim()`).
