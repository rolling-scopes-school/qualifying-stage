# Task RSS-QS-4-3-4: Authenticated User Auth Dialog URL Guard (15 points)

## Description

Restrict Auth dialog access for users with a valid active session, including direct URL deep links such as `?auth=login` / `?auth=register`, and provide clear user feedback.

## Acceptance Criteria

- **UI Guard:** If a user with a valid active session attempts to open the Auth dialog via header/menu controls, the Auth modal SHOULD NOT open.
- **Deep Link Guard:** If a logged-in user opens a URL with an auth modal parameter (e.g., `?auth=login` or `?auth=register`), the Auth modal SHOULD NOT open.
- **URL Cleanup:** The URL address bar should automatically revert/clear the auth parameter without a full page reload.
- **User Feedback:** A Snackbar notification should inform the user that they are already authenticated.
- **Session Rules Alignment:** "Valid active session" follows the Story 4 session persistence and 5-minute expiration rules.
