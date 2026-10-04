# Task RSS-QS-4-1-2: Email/Password Authentication Flow and UI States (20 points)

## Description

Connect the Login and Registration forms to Firebase Email/Password Authentication with pending UI locks, loading feedback, and success/error handling.

## Acceptance Criteria

- **Submit Dispatches Firebase Operation:** A valid form submission triggers the corresponding Firebase email/password sign-in or account-creation operation. Login uses the user's email address and password.
- **Registration Profile Name:** When creating an account, save the registration form's username as the Firebase user's `displayName`.
- **Prevent Duplicate Authentication:** While an authentication operation is pending, disable all authentication actions and form inputs so the user cannot submit another request.
- **Keep Dialog Open while Pending:** While an authentication operation is pending, the user cannot close the Auth dialog using its close button, the backdrop, or the Escape key.
- **Authentication Outcome:** On failure, keep the dialog open, unlock the controls, and allow the user to retry. On success, create the app session according to [User Session Persistence & Expiration](RSS-QS-4-3-2-session-persistence-expiration.md), apply the authenticated UI state, and close the dialog.

- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](../story-3/common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](../story-3/common-snackbar-notification-requirements.md). This is a mandatory criterion.
