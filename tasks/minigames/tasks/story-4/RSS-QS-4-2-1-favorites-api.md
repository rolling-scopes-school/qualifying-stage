# Task RSS-QS-4-2-1: Add / Remove Favorites API Integration (15 points)

## Description

Implement add-to-favorites and remove-from-favorites actions via backend API requests with authorization checks and UI state updates.

## API Endpoint Hint

- **Method and endpoint:** `POST /api/games/{gameSlug}/favorite`
- **Path parameter:** `gameSlug` — the selected game's slug (for example, `tukoni-forest-keepers`).
- **Request body:** send the active app-session user's email as JSON:

  ```json
  {
    "userEmail": "student@rs.school"
  }
  ```

- **Successful response:** `200`, with the updated state in `data.isFavorited` and `data.likesCount`.
- **Toggle behavior:** this single endpoint both adds and removes a favorite. Every successful request flips the state; there are no separate add/remove endpoints. Do not automatically retry a request whose outcome is unknown, because a second POST can undo the first.
- **Identity:** use the email from the active app session. The backend contract does not require a Firebase bearer token; the client session guard remains responsible for deciding whether the request may be sent.
- **Initial state:** When opening Game Details in authenticated mode, request `GET /api/games/{gameSlug}?userEmail={email}` and initialize the favorite control from `data.isLikedByCurrentUser`. URL-encode the email query value. This field represents whether the current user has favorited the game.

## Acceptance Criteria

- **Authorization Check:** Favorites toggle is available ONLY to authenticated users. If a guest clicks the control, open the Auth modal and show a Snackbar warning.
- **API Request:** Toggling favorites dispatches the corresponding backend API request for the current game and user identity required by the API contract.
- **Button Locking & Loading:** While the request is pending, the favorites control is locked and shows loading feedback.
- **Server-Driven UI Update:** Initialize the state from the personalized Game Details response's `data.isLikedByCurrentUser`, then update it from the favorite POST response's `data.isFavorited` and `data.likesCount`. Do not rely on optimistic-only local guesswork without server confirmation.
- **No Duplicate Toggle:** Prevent duplicate in-flight requests and do not automatically replay a favorite toggle after a timeout or other ambiguous network failure.

- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](../story-3/common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](../story-3/common-snackbar-notification-requirements.md). This is a mandatory criterion.
