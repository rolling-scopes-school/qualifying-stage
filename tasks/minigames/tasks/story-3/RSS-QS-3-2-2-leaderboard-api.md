# Task RSS-QS-3-2-2: Top Players Leaderboard API Integration (25 points)

## Description

Load and render the Home page Top Players leaderboard from the backend REST API.

## Acceptance Criteria

- **API Data Fetching:** Leaderboard rows are fetched from the backend API endpoint for top players.
- **Dynamic Table Rendering:** Rank, player name, score/stats, and other required leaderboard fields are rendered from the response.
- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](common-snackbar-notification-requirements.md). This is a mandatory criterion.
- **Empty State:** If the API returns an empty leaderboard list, show an empty-state placeholder instead of a broken table.
