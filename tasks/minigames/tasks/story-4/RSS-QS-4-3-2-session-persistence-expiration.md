# Task RSS-QS-4-3-2: User Session Persistence & Expiration in LocalStorage (20 points)

## Description

Implement user session persistence in `localStorage`. Store non-sensitive user profile data upon authentication, maintain authenticated state across page refreshes for 5 minutes, and handle automatic session expiration.

## Acceptance Criteria

- **LocalStorage Profile Storage:** Upon successful authentication (login or registration), store non-sensitive user profile data in `localStorage` (username and avatar URL if available). Storing passwords in `localStorage` is strictly prohibited.
- **Session Timestamp & Persistence:** Save an authorization timestamp alongside user data. On page refresh or when invoking authorized features, if less than 5 minutes (300 seconds) have passed since authorization, the authenticated session persists, and all authorized features remain accessible.
- **5-Minute Session Expiration & UI Reset:** If 5 minutes (300 seconds) or more have elapsed since authorization (checked upon page refresh or when invoking authorized features):
  - User data in `localStorage` should be cleared.
  - The session expires and the application immediately transitions back to guest mode (restoring Login and Registration controls in the header and mobile menu).
  - A Snackbar notification should be displayed to inform the user that their session has expired and re-authentication is required.
  - Attempting an authorized feature (favorites, comments, likes) with an expired session should open the Auth modal dialog.

> **Reviewer Note:**
> To test 5-minute session expiration without waiting, reviewers can open DevTools (Application tab -> Local Storage), manually decrease the saved timestamp value by 300+ seconds, and refresh the page or click an authorized feature button.
