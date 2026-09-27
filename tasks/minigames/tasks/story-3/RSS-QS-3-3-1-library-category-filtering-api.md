# Task RSS-QS-3-3-1: Library Category Filtering via API (35 points)

## Description

Implement Library category filtering by sending filter criteria to the backend API (no client-side-only filtering of a full preloaded list as the primary mechanism).

## Acceptance Criteria

- **Server-Side Filtering:** Changing the active category dispatches a backend API request with the selected category parameter.
- **UI Sync:** The active category chip/control visually reflects the selected filter.
- **Results Update:** The game cards list updates according to the API response for the selected category.
- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](common-snackbar-notification-requirements.md). This is a mandatory criterion.
- **Default State:** An "All Games" (or equivalent default) category requests the unfiltered/default games list from the API.
- **No Client-Side-Only Filtering Penalty Path:** Filtering must not be implemented solely by filtering a once-fetched full dataset on the client when the API supports category query parameters.
