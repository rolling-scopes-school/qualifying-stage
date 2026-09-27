# Task RSS-QS-3-3-2: Library Game Sorting via API (35 points)

## Description

Implement Library sorting by sending sort parameters to the backend API.

## Acceptance Criteria

- **Server-Side Sorting:** Changing the sort control dispatches a backend API request with the selected sort parameter.
- **UI Sync:** The sort dropdown/control reflects the active sort option.
- **Results Update:** The game cards list order updates according to the API response.
- **Combination with Filters:** Sort works together with the active category filter (both parameters are sent in the same or coordinated API requests).
- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](common-snackbar-notification-requirements.md). This is a mandatory criterion.
- **No Client-Side-Only Sorting Penalty Path:** Sorting must not be implemented solely by sorting a full client-side array when the API supports sort query parameters.
