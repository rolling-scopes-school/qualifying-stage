# Task RSS-QS-4-1-3: Firebase Project, Email/Password Provider, and SDK Setup (50 points)

## Description

Configure a personal Firebase project and integrate the Firebase SDK into the application frontend. Complete this setup before implementing the Email/Password authentication flow in [RSS-QS-4-1-2](RSS-QS-4-1-2-auth-registration-api.md).

## Acceptance Criteria

- **Firebase Console Project Setup:** Create and configure a personal project in the [Firebase Console](https://console.firebase.google.com/).
- **Authentication Setup:** Email/Password authentication provider is enabled in Firebase Console.
- **Frontend Integration:** Firebase SDK is initialized and integrated into the TypeScript project codebase.

> **Hint:** Firebase Authentication is the identity provider; it does not have a Firebase Console setting for the MiniGames app's 5-minute session lifetime. Keep the app-session TTL separate from Firebase persistence, and call Firebase `signOut` when that app session expires or the user logs out. The client-side TTL is an educational cross-check requirement, not production-grade session security.
