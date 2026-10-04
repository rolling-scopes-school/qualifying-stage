# Task RSS-QS-4-1-4: Google OAuth Account Authorization (40 points)

## Description

Implement Google account sign-in using Firebase Authentication.

## Acceptance Criteria

- **Google Provider Enabled:** Google sign-in provider is enabled in the Firebase project and configured in the frontend.
- **Google Sign-In Control:** Auth UI provides a working Google account authorization action.
- **Prevent Duplicate Authentication:** While Google authentication is pending, disable all authentication actions and form inputs so another authentication request cannot be started.
- **Keep Dialog Open while Pending:** While Google authentication is pending, the user cannot close the Auth dialog using its close button, the backdrop, or the Escape key.
- **Successful Authorization:** On success, create the same app session used by Email/Password authentication according to [User Session Persistence & Expiration](RSS-QS-4-3-2-session-persistence-expiration.md), update the UI to the authenticated state, and close the Auth dialog.
- **Failed / Canceled Authorization:** If Google authentication fails or the user closes/cancels the provider flow, keep the Auth dialog open and re-enable its controls.

- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](../story-3/common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](../story-3/common-snackbar-notification-requirements.md). This is a mandatory criterion.

> **Hint:** Google OAuth through Firebase establishes the same Firebase identity used by Email/Password login. After success, create the same separate 5-minute app session.
