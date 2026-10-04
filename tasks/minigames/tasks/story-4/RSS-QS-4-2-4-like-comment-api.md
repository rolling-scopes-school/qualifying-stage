# Task RSS-QS-4-2-4: Like Comment API Integration (15 points)

## Description

Implement comment liking functionality via API request with authorization checks and server-driven state updates.

## Acceptance Criteria

- **Authorization Check:** Comment liking is available ONLY to authenticated users. If an unauthenticated guest clicks the like button, open the Auth modal dialog and show a Snackbar notification warning.
- **Button Locking & Loading:** Clicking like locks the button (disabled state) and displays a loading indicator.
- **Server-Driven State Update:** The comment like count and active like button state update strictly according to backend API response data.

- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](../story-3/common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](../story-3/common-snackbar-notification-requirements.md). This is a mandatory criterion.
