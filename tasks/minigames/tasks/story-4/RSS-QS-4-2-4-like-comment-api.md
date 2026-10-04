# Task RSS-QS-4-2-4: Like Comment API Integration (15 points)

## Description

Implement comment liking functionality via API request with authorization checks and server-driven state updates.

## API Endpoint Hint

- **Method and endpoint:** `POST /api/comments/{commentId}/like`
- **Path parameter:** `commentId` — the comment UUID returned by `GET /api/games/{gameSlug}/comments`.
- **Request body:** send the active app-session user's email as JSON:

  ```json
  {
    "userEmail": "student@rs.school"
  }
  ```

- **Successful response:** `200`, with `data.isLikedByCurrentUser` and `data.likesCount` for the affected comment.
- **Toggle behavior:** this endpoint likes or unlikes with the same POST; each successful request flips the state. Prevent duplicate in-flight requests and do not automatically retry a request with an unknown outcome.
- **Identity:** use the email from the active app session. The backend contract does not require a Firebase bearer token; the client session guard controls access to the mutation.

## Acceptance Criteria

- **Authorization Check:** Comment liking is available ONLY to authenticated users. If an unauthenticated guest clicks the like button, open the Auth modal dialog and show a Snackbar notification warning.
- **Button Locking & Loading:** Clicking like locks the button (disabled state) and displays a loading indicator.
- **Server-Driven State Update:** The comment like count and active like button state update strictly according to backend API response data.
- **Personalized Initial State:** The comments list used to render the buttons is fetched with the active user's `userEmail`, so each comment's `isLikedByCurrentUser` value initializes the button correctly. Guest requests omit `userEmail`.
- **No Duplicate Toggle:** Do not issue another like toggle while the first request is pending or automatically replay it after an ambiguous network failure.

- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](../story-3/common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](../story-3/common-snackbar-notification-requirements.md). This is a mandatory criterion.
