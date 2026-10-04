# Task RSS-QS-4-3-3: User Logout Functionality & Guest Mode Reset (15 points)

## Description

Implement user logout functionality via the header and mobile burger menu controls, clearing session data and returning the application to guest mode.

## Acceptance Criteria

- **Logout Controls Availability:** After successful authentication, Logout buttons are accessible in both the main site header and the mobile burger menu (according to the Figma layout).
- **LocalStorage Data Cleanup:** Clicking the Logout button clears user profile and session data stored in `localStorage` (if implemented).
- **Guest Mode Transition:** The application transitions immediately back to unauthenticated guest mode, restoring Login and Registration buttons in the header and mobile menu with full capability to authenticate again.
- **Access Restriction:** Upon logging out, all features restricted to authenticated users (adding games to favorites, submitting comments, liking comments) become inaccessible/restricted according to guest access rules.

- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](../story-3/common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](../story-3/common-snackbar-notification-requirements.md). This is a mandatory criterion.

> **Hint:** Logout must end both layers of state: clear the MiniGames app-session data from `localStorage` and call Firebase `signOut`. Clearing only the app-session record can leave Firebase's persisted identity active and allow it to be restored on a later reload.
