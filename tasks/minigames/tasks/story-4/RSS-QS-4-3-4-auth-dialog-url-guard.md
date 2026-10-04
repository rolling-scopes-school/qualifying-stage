# Task RSS-QS-4-3-4: Authenticated User Auth Dialog URL Guard (15 points)

## Description

Guard every Auth dialog entry point using the active app session, including UI actions, direct URLs, and browser history navigation.

## Acceptance Criteria

- **Guard All Entry Points:** If a user with a valid app session attempts to open Auth from any UI control, URL, or browser history navigation, do not open the Auth dialog.
- **Clean the URL:** Remove only the `auth` parameter, preserve the current path, other query parameters, and hash, and update the current history entry through the SPA router without a page reload or an extra Back-button entry.
- **User Feedback:** Show one Snackbar explaining that the user is already authenticated.
- **Expired or Invalid Session:** Apply the session recovery rules before deciding whether to block Auth. A user whose session is expired or invalid is a guest; after recovery, allow an Auth URL such as `?auth=login` or `?auth=register` to open.
- **Game Details State:** When Auth replaces Game Details after a protected action, preserve the game URL/state and restore Game Details when Auth closes. Follow the session transition and no-auto-retry behavior in [App Session Persistence, Validation & Expiration](RSS-QS-4-3-2-session-persistence-expiration.md).
- **Browser History:** Back and Forward restore the matching Auth or Game Details state through the Story 3 SPA router without a full page reload.
