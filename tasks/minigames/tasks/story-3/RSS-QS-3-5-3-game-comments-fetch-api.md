# Task RSS-QS-3-5-3: Game Comments Fetching API Integration (20 points)

## Description

Fetch and render the latest game comments and total comment count in the Game Details dialog from the backend API (read-only in this story).

## Acceptance Criteria

- **Latest Comments Fetch:** Load comments for the opened game from the API using a limit of 3 latest comments (e.g. `?limit=3`) unless the API specification defines an equivalent contract.
- **Comments List Rendering:** Render author name, comment text, likes count, and created time for each returned comment.
- **Relative Time Formatting:** Convert API timestamps to a human-readable relative-time string before display:
  - `< 1 minute` → `just now`
  - `1–59 min` → `1 min ago` … `59 min ago`
  - `1–23 hrs` → `1 hour ago` … `23 hours ago`
  - `1–6 days` → `1 day ago` … `6 days ago`
  - `3–4 weeks` → `1 week ago` … `3 weeks ago`
  - `1–11 months` → `1 month ago` … `11 months ago`
  - `≥ 1 year` → `1 year ago` / `2 years ago` / … (full-year increments)
- **Total Count Header:** Retrieve the total number of comments for the game and display the exact count in the comments section header (e.g. `Comments (12)`).
- **Loading & Error States:** Comments block uses skeleton/loading and error/empty feedback consistent with global UI rules.
- **Guest-Safe Read-Only Behavior:** Comment posting, liking, and other authenticated mutations are out of scope for this task and remain disabled/locked for guests until Story 4.
