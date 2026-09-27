# Task RSS-QS-3-2-1: Library Game Cards List API Integration (15 points)

## Description

Load and render the Library page game cards list from the backend REST API. The list must update according to the backend response and request a fixed page size of 6 cards.

## API Endpoint Hint

- **Endpoint:** `GET /api/games`
- **Required query parameter for this task:** `limit=6`
- **Behavior:** the cards list is rendered from the API response items
- **Example:** `/api/games?limit=6`

## Acceptance Criteria

- **API Data Fetching:** Game cards are loaded from the backend API.
- **Response-Driven List:** The cards list updates according to the backend response.
- **Dynamic Rendering:** Each card renders the required fields from the API response (for example title, image, description/rating/likes as applicable to the existing Library cards UI).
- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](common-snackbar-notification-requirements.md). This is a mandatory criterion.
