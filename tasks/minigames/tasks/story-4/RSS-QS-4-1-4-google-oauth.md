# Task RSS-QS-4-1-4: Google OAuth Account Authorization (40 points)

## Description

Implement user authentication and registration using Google Account OAuth via Firebase Google Auth Provider.

## Acceptance Criteria

- **Google Provider Enabled:** Google sign-in provider is enabled in the Firebase project and configured in the frontend.
- **Google Sign-In Control:** Auth UI provides a working Google account authorization action.
- **Successful Authorization:** Successful Google sign-in establishes an authenticated application session and updates the UI to the authenticated state.
- **Failed / Canceled Authorization:** If Google authentication fails or is closed/canceled by the user, re-enable UI controls and keep the Auth modal open.

- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](../story-3/common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](../story-3/common-snackbar-notification-requirements.md). This is a mandatory criterion.

> **Hint:** Google OAuth through Firebase establishes the same Firebase identity used by Email/Password login. After success, create the same separate 5-minute app session.
