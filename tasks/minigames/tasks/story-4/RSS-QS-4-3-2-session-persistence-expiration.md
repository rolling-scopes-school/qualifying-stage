# Task RSS-QS-4-3-2: App Session Persistence, Validation & Expiration (20 points)

## Description

Implement the client-side app session described in the [Story 4 Architecture Note](../../story-4.md). Persist the minimum profile data needed by the UI and API, restore a still-valid session after reload, and return the app to Guest Mode when the session expires or its stored data is invalid. This app session is distinct from Firebase Authentication's persisted identity.

## Acceptance Criteria

- **Namespaced Storage Key:** Store the session as one JSON object under a stable, project-specific `localStorage` key, for example `minigames:<unique-project-id>:app-session`; do not use a generic key such as `user`, `auth`, or `session`. Document the exact key in the project README or PR description so reviewers can inspect it without relying on implementation details.
- **Session Data:** On successful authentication, store `displayName`, `email`, `authenticatedAt` (the numeric millisecond timestamp returned by `Date.now()`), and `avatarUrl` only when available. Use the same profile values for Email/Password and Google sign-in. Do not store passwords, Firebase tokens, or unrelated user data.
- **Restore After Reload:** On startup, parse and validate the stored object. If it is valid and not expired under the Architecture Note's session policy, restore the authenticated UI without changing `authenticatedAt`; reloading or using the app should not extend the session lifetime.
- **Invalid Stored Data:** If the value is not valid JSON or is missing required fields or has fields of the wrong type, remove only this app's session key, call Firebase `signOut`, and start in Guest Mode. The application must not crash or restore an authenticated state from Firebase's `currentUser` alone.
- **Session Expiration:** Check the session at startup, when the page becomes active again, before page or dialog navigation, and before every protected action. When expired, remove only the app's session key, call Firebase `signOut`, and immediately switch the UI to Guest Mode. Show one Snackbar for the expiration event.
- **Protected Action after Expiration:** If session is expired do not send the attempted favorite, comment, or like request. Preserve the current Game Details state and URL, but show Auth instead of Game Details so only one dialog is active. If authentication succeeds, close Auth and restore Game Details in authenticated mode. If Auth is canceled or closed, restore Game Details in Guest Mode. Do not automatically repeat the blocked action; the user can retry it explicitly.
- **Page or Dialog Navigation after Expiration:** Continue the requested public navigation in Guest Mode.

> **Reviewer Note:** Reviewers can inspect the documented key in DevTools (Application -> Local Storage), change `authenticatedAt` to a timestamp older than the configured session lifetime, then reload the page or try a protected action.
