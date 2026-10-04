# Task RSS-QS-3-3-1: Game Details Modal API Integration (30 points)

## Description

Load Game Details modal content from the backend API when the dialog is opened and render hero, info, and related sections from the response.

## API Endpoint Hint

- **Endpoint:** `GET /api/games/{gameSlug}`
- **Path parameter:** `gameSlug` — kebab-case game identifier (example: `tukoni-forest-keepers`)
- **Optional query parameter:** `userEmail` — when supplied, `data.isLikedByCurrentUser` reflects whether this user has favorited the game. Story 4 uses this value to initialize the favorite control; omit it for guests.
- **Example:** `/api/games/tukoni-forest-keepers?userEmail=student%40rs.school`

## Acceptance Criteria

- **API Data Fetching:** Opening Game Details dispatches `GET /api/games/{gameSlug}` for the selected game. In authenticated mode, include the active user's URL-encoded `userEmail` query parameter and use `data.isLikedByCurrentUser` as the initial favorite state.
- **Dynamic Rendering:** Title, description, media, badges, ratings/records, and other required fields are rendered from the API response.
- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](common-snackbar-notification-requirements.md). This is a mandatory criterion.
