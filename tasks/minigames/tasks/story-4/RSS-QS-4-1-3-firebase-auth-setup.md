# Task RSS-QS-4-1-3: Firebase Workspace & Authentication Setup (50 points)

## Description

Configure a personal Firebase project workspace and integrate Firebase Authentication into the application frontend for user registration and credential management.

## Acceptance Criteria

- **Firebase Console Project Setup:** The student creates and configures a personal workspace project in the [Firebase Console](https://console.firebase.google.com/).
- **Authentication Setup:** Email/Password authentication provider is enabled in Firebase Console.
- **Frontend Integration:** Firebase SDK is initialized and integrated into the TypeScript project codebase.
- **User Data Storage:** User registration requests create and persist accounts within the Firebase Authentication database.
- **Credential Validation:** Registered users can log in using their credentials (username/password).

> **Hint:** Firebase Authentication is the identity provider; it does not have a Firebase Console setting for the MiniGames app's 5-minute session lifetime. Keep the app-session TTL separate from Firebase persistence, and call Firebase `signOut` when that app session expires or the user logs out. The client-side TTL is an educational cross-check requirement, not production-grade session security.
