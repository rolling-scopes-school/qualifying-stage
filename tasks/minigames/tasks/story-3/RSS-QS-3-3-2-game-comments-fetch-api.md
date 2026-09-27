# Task RSS-QS-3-3-2: Game Comments Fetching API Integration (30 points)

## Description

Fetch and render the latest game comments and total comment count in the Game Details dialog from the backend API (read-only in this story).

## API Endpoint Hint

- **Endpoint:** `GET /api/games/{gameSlug}/comments`
- **Query parameters:**
  - `limit=3` — return the 3 latest comments for this story
  - `sort=newest` — recommended for “latest comments” ordering
- **Example:** `/api/games/tukoni-forest-keepers/comments?limit=3&sort=newest`

## Acceptance Criteria

- **Latest Comments Fetch:** Load comments for the opened game from `GET /api/games/{gameSlug}/comments` with `limit=3`.
- **Comments List Rendering:** Render author name, comment text, likes count, and created time for each returned comment.
- **Relative Time Formatting:** Convert API timestamps to a human-readable relative-time string before display:
  - `< 1 minute` → `just now`
  - `1–59 min` → `1 min ago` … `59 min ago`
  - `1–23 hrs` → `1 hour ago` … `23 hours ago`
  - `1–6 days` → `1 day ago` … `6 days ago`
  - `1–3 weeks` → `1 week ago` … `3 weeks ago`
  - `1–11 months` → `1 month ago` … `11 months ago`
  - `≥ 1 year` → `1 year ago` / `2 years ago` / … (full-year increments)
- **Total Count Header:** Retrieve the total number of comments for the game and display the exact count in the comments section header (e.g. `Comments (12)`).
- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](common-snackbar-notification-requirements.md). This is a mandatory criterion.
- **Guest-Safe Read-Only Behavior:** Comment posting, liking, and other authenticated mutations are out of scope for this task and will be implemented in Story 4.
