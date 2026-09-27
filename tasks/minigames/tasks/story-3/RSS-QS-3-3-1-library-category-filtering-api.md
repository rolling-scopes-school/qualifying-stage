# Task RSS-QS-3-3-1: Library Category Filtering via API (35 points)

## Description

Implement Library category filtering by loading categories from the backend and sending the selected category to the games list API (no client-side-only filtering of a full preloaded list as the primary mechanism).

## API Endpoint Hint

- **Categories endpoint:** `GET /api/categories`
- **Games list endpoint:** `GET /api/games`
- **Games query parameter:** `category=<category-value>`
- **Allowed category values (API):** `all`, `puzzle`, `card`, `match`, `farm`, `strategy`, `arcade` (`all` means no filter)
- **Examples:**
  - `/api/categories`
  - `/api/games?category=puzzle&sort=rating-desc&page=1&limit=6`

## Acceptance Criteria

- **API Data Fetching:** Category chips/controls are loaded from the backend API.
- **Dynamic Rendering:** The list of categories is rendered from the API response.
- **Default State:** On initial load, the active category chip is the one with `isDefault: true` from the API response.
- **UI Sync:** The active category chip/control visually reflects the selected filter.
- **Server-Side Filtering:** Changing the active category dispatches a backend `GET /api/games` request with the selected `category` parameter and updates the Library game cards list from that response.
- **Combination with Sort:** Sort works together with the active category filter (both parameters are sent in the same API request).
- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](common-snackbar-notification-requirements.md). This is a mandatory criterion.
