# Task RSS-QS-3-5-1: Game Details Modal API Integration (15 points)

## Description

Load Game Details modal content from the backend API when the dialog is opened and render hero, info, and related sections from the response.

## Acceptance Criteria

- **API Data Fetching:** Opening Game Details dispatches a backend request for the selected game (by id/slug as defined by the API).
- **Dynamic Rendering:** Title, description, media, badges, ratings/records, and other required fields are rendered from the API response (not permanent hardcoded game content for Story 3 final behavior).
- **Loading State:** While the request is pending, skeleton placeholders are shown inside the modal content areas.
- **Error Handling:** Network/server failures show an error state inside the modal or via Snackbar with a way to retry/close cleanly.
