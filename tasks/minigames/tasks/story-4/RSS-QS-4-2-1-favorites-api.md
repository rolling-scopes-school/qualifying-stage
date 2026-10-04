# Task RSS-QS-4-2-1: Add / Remove Favorites API Integration (15 points)

## Description

Implement add-to-favorites and remove-from-favorites actions via backend API requests with authorization checks and UI state updates.

## Acceptance Criteria

- **Authorization Check:** Favorites toggle is available ONLY to authenticated users. If a guest clicks the control, open the Auth modal and show a Snackbar warning.
- **API Request:** Toggling favorites dispatches the corresponding backend API request for the current game and user identity required by the API contract.
- **Button Locking & Loading:** While the request is pending, the favorites control is locked and shows loading feedback.
- **Server-Driven UI Update:** Favorites active/inactive state updates according to the API response, not optimistic-only local guesswork without server confirmation.

- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](../story-3/common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](../story-3/common-snackbar-notification-requirements.md). This is a mandatory criterion.
