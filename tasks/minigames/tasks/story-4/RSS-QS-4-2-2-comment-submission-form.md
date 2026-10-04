# Task RSS-QS-4-2-2: Comment Submission Form & Auto-expand Textarea (20 points)

## Description

Implement the comment submission form inside the Game Details dialog with an auto-expanding textarea, submit via Enter key or button, and API comments list refresh.

## API Endpoint Hint

- **Method and endpoint:** `POST /api/games/{gameSlug}/comments`
- **Path parameter:** `gameSlug` — the selected game's slug (for example, `tukoni-forest-keepers`).
- **Request body:** use the email and display name from the active app session, plus the textarea value:

  ```json
  {
    "userEmail": "student@rs.school",
    "authorName": "ForestDweller",
    "text": "Such a calming little game!"
  }
  ```

- **Request constraints:** `authorName` is the authenticated profile's `displayName` (2–30 characters); `text` must contain 1–500 characters after trimming. The API returns `201` with the created comment in `data`; this POST response does not include `meta.totalComments`.
- **After success:** fetch `GET /api/games/{gameSlug}/comments?...&userEmail={email}`. Use this GET response's `data` for the visible comments and its `meta.totalComments` for the heading count. The GET metadata contains the full comment count even though only three comments are returned. URL-encode the email query value.
- **Identity:** `userEmail` comes from the active app session. The backend does not require a Firebase bearer token; the client session guard controls access to this mutation.

## Acceptance Criteria

- **Initial State:** When opening the Game Details dialog, the comment text field is cleared.
- **Auto-Expanding Textarea:** Textarea expands vertically as text is typed according to the design layout. Upon reaching maximum height, an internal vertical scrollbar appears inside the textarea.
- **Submission Trigger:** Comment submission is triggered by clicking the Send button or pressing the `Enter` key (without `Shift`).
- **Input Locking during Request:** While sending the comment API request, the textarea input and submit button are locked (disabled state).
- **Input Validation & Safe Rendering:** Trim the submitted text and reject empty or over-500-character values. The API sanitizes stored text server-side; render returned comment text as text (never inject it as HTML) and do not rely on client-side sanitization as the security boundary.
- **Failure Recovery:** If the submission request fails or returns an error, the form fields and submit button are unlocked, and the typed comment text SHOULD NOT be cleared from the textarea, allowing the user to retry.
- **Post-Submission Reset:** After a successful `201` response, clear the textarea and fetch the updated three latest comments with `limit=3`, `sort=newest`, and the active user's `userEmail`; update the section header from `meta.totalComments`. If the POST fails, retain the typed text for retry. If the POST succeeds but the follow-up GET fails, keep the form cleared (the comment was created), retain the currently displayed comments/count, and show refresh error feedback without resubmitting the comment.
- **Access Control:** Comment posting is available ONLY to authenticated users. For guest/unauthenticated users, the comment input block should be locked/disabled or hidden.
- **Authenticated User Avatar in Comment Form:** The comment submission form displays the **uppercase first letter** of the authenticated user's username.

- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](../story-3/common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](../story-3/common-snackbar-notification-requirements.md). This is a mandatory criterion.
