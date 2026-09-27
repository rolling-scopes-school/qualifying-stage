# Task RSS-QS-3-5-1: Game Details Modal API Integration (30 points)

## Description

Load Game Details modal content from the backend API when the dialog is opened and render hero, info, and related sections from the response.

## Acceptance Criteria

- **API Data Fetching:** Opening Game Details dispatches a backend request for the selected game (by id/slug as defined by the API).
- **Dynamic Rendering:** Title, description, media, badges, ratings/records, and other required fields are rendered from the API response (not permanent hardcoded game content for Story 3 final behavior).
- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](common-snackbar-notification-requirements.md). This is a mandatory criterion.
- **Error Handling:** Network/server failures show an error state inside the modal (and/or via Snackbar) with a way to retry/close cleanly.
