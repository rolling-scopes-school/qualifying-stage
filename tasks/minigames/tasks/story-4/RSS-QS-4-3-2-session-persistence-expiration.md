# Task RSS-QS-4-3-2: User Session Persistence & Expiration in LocalStorage (20 points)

## Description

Implement a short-lived client-side app session in `localStorage`. Store non-sensitive user profile data upon authentication, maintain the app's authenticated UI state across page refreshes for 5 minutes, and handle automatic session expiration. This app session is distinct from Firebase Authentication's own persisted identity state.

## Acceptance Criteria

- **LocalStorage Profile Storage:** Upon successful authentication (login or registration), store non-sensitive user profile data in `localStorage` (username and avatar URL if available). Storing passwords in `localStorage` is strictly prohibited.
- **Session Timestamp & Persistence:** Save an authorization timestamp alongside user data. On page refresh or when invoking authorized features, if less than 5 minutes (300 seconds) have passed since authorization, the authenticated session persists, and all authorized features remain accessible.
- **5-Minute Session Expiration & UI Reset:** If 5 minutes (300 seconds) or more have elapsed since authorization (checked upon page refresh or when invoking authorized features):
  - User data in `localStorage` should be cleared.
  - Firebase Authentication should be signed out so its persisted identity does not restore the expired app session.
  - The session expires and the application immediately transitions back to guest mode (restoring Login and Registration controls in the header and mobile menu).
  - A Snackbar notification should be displayed to inform the user that their session has expired and re-authentication is required.
  - Attempting an authorized feature (favorites, comments, likes) with an expired session should open the Auth modal dialog.

> **Hint:** `localStorage` is controlled by the client and can be inspected or modified, so this mechanism is not a security boundary and must not contain passwords or Firebase tokens. The 5-minute TTL is intentionally short to make the educational cross-check convenient; it is not a recommended production session lifetime. Firebase identity lifetime and app-session lifetime are separate: use the app session for UI/feature guards, and call Firebase `signOut` on expiry. To make expiration automatic while the app is open, schedule a check for the stored expiry time; always re-check on startup and before protected actions as well.

> **Reviewer Note:**
> To test 5-minute session expiration without waiting, reviewers can open DevTools (Application tab -> Local Storage), manually decrease the saved timestamp value by 300+ seconds, and refresh the page or click an authorized feature button.
