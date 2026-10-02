# Task RSS-QS-4-1-4: Google OAuth Account Authorization (40 points)

## Description

Implement user authentication and registration using Google Account OAuth via Firebase Google Auth Provider.

## Acceptance Criteria

- **Google Provider Enabled:** Google sign-in provider is enabled in the Firebase project and configured in the frontend.
- **Google Sign-In Control:** Auth UI provides a working Google account authorization action.
- **Successful Authorization:** Successful Google sign-in establishes an authenticated application session and updates the UI to the authenticated state.
- **Failed / Canceled Authorization:** If Google authentication fails or is closed/canceled by the user, show an error Snackbar message, re-enable UI controls, and keep the Auth modal open.
