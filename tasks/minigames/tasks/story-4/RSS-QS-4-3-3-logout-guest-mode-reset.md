# Task RSS-QS-4-3-3: User Logout Functionality & Guest Mode Reset (15 points)

## Description

Implement logout through the header and mobile menu, using the same guest-mode reset as session expiration.

## Acceptance Criteria

- **Logout Controls:** Show a working Logout control in the desktop header and mobile menu while an app session is active.
- **End the App Session:** On logout, remove only the namespaced session key defined in [App Session Persistence, Validation & Expiration](RSS-QS-4-3-2-session-persistence-expiration.md), call Firebase `signOut`, and immediately transition to Guest Mode. Do not clear unrelated `localStorage` data.
- **Reset User-Specific UI:** Restore Login and Registration controls and remove or refresh user-specific UI state, including favorite and comment-like state. Keep public page content open; if Game Details is open, show its Guest Mode state.
- **Guest Access:** After logout, protected actions follow the guest access behavior defined in the relevant interaction tasks.

- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](../story-3/common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](../story-3/common-snackbar-notification-requirements.md). This is a mandatory criterion.
  > **Sign-Out Error:** If Firebase `signOut` fails, keep the app in Guest Mode, show error feedback, and do not restore authenticated UI from Firebase's `currentUser` alone.
