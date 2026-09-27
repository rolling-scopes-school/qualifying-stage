# Task RSS-QS-3-2-1: Hero Carousel / Slider API Integration (15 points)

## Description

Replace static/mock carousel data on the Home page with live backend API data and render slides from the featured games response.

## API Endpoint Hint

- **Endpoint:** `GET /api/games`
- **Required query parameter:** `featured=true`
- **Behavior:** when `featured=true`, the API returns the featured games list for the Home slider and ignores other list parameters.
- **Example:** `/api/games?featured=true`

## Acceptance Criteria

- **API Data Fetching:** Featured games are loaded from the backend API.
- **Dynamic Rendering:** Slider cards render title, image, and other required fields from the API response.
- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](common-snackbar-notification-requirements.md). This is a mandatory criterion.
