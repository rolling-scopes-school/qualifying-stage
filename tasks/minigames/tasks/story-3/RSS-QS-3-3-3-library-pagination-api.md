# Task RSS-QS-3-3-3: Library Pagination via API (40 points)

## Description

Implement Library pagination through backend API `page` / `limit` parameters and build pagination controls dynamically from response metadata.

## API Endpoint Hint

- **Endpoint:** `GET /api/games`
- **Query parameters:**
  - `page=<page-number>` (page number ≥ 1, default `1`)
  - `limit=<page-size>`
- **Response metadata used by UI:** `page`, `totalPages`
- **Example:** `/api/games?page=2&limit=6&category=all&sort=rating-desc`

## Acceptance Criteria

- **Controls from Metadata:** Pagination UI (current page, total pages, disabled prev/next states) is driven by API response metadata (`page`, `totalPages`). The pagination component is built dynamically from the backend response.
  - Even if the games list is empty, show page `1`, the pagination controls (left/right arrows), and the Data Not Found banner for the list area.
  - If `totalPages` is greater than the visible page-button limit from the design (**4** on desktop/tablet, **3** on mobile), use the visible-window logic described in Story 2.
  - If `totalPages` is smaller than those limits, render only the actual number of pages (for example, only 2 page buttons when `totalPages = 2`).
- **Server-Side Pagination:** Changing page dispatches a backend `GET /api/games` request with the selected `page`.
- **Results Update:** The game cards list shows only the items returned for the requested page.
- **Reset Behavior:** Changing category filter or sort resets pagination to page `1` and requests the first page from the API.
- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](common-snackbar-notification-requirements.md). This is a mandatory criterion.
