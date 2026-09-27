# Task RSS-QS-3-2-3: Library Game Sorting via API (35 points)

## Description

Implement Library sorting by sending sort parameters to the backend games list API and updating the cards list from the response.

## API Endpoint Hint

- **Endpoint:** `GET /api/games`
- **Query parameter:** `sort=<sort-value>`
- **Allowed sort values (API):** `rating-desc`, `rating-asc`, `name-asc`, `name-desc`
- **Example:** `/api/games?sort=rating-desc&category=all&page=1&limit=6`

## Acceptance Criteria

- **Default Sort:** The default sort value is `rating-desc`.
- **UI Sync:** The sort dropdown/control reflects the active sort option.
- **Server-Side Sorting:** Changing the sort control dispatches a backend `GET /api/games` request with the selected `sort` parameter and updates the Library game cards list from that response.
- **Combination with Filters:** Sort works together with the active category filter (both parameters are sent in the same API request).
- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](common-snackbar-notification-requirements.md). This is a mandatory criterion.
