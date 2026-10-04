# MiniGames Story 4

Total: **423 points**

## Goal

- Integrate Authentication (Email/Password & Firebase Google OAuth) with form validation, input locking during requests, and state persistence.
- Handle interactive features for authenticated users (favorite games toggle, comment submissions, comment likes).
- Implement authenticated user header/profile UI, `localStorage` session lifetime (5 minutes), logout/guest reset, and Auth dialog access guards for logged-in users.
- Set up unit testing tooling (`vitest` or `jest`) and scripts in `package.json`, achieve **80%+ code coverage** across logic files, and document test exclusions with mandatory comments.

### Architecture Note for Auth & API

- **Firebase Authentication SDK** is used as the Identity Provider for user authentication (Email/Password and Google OAuth). Firebase authentication persistence and the MiniGames client-side app session are separate concerns: Firebase establishes the user's identity, while the app session controls whether the UI treats the user as authenticated.
- **Client-Side Authorization Management:** Backend REST API endpoints are public and respond identically to all requests without validating session tokens. Students should implement frontend logic to control feature availability and restrict unauthorized API calls based on the active client session state.
- **App Session Lifetime:** The app session is maintained on the client for **5 minutes** from successful authentication, then the frontend transitions back to Guest Mode. This intentionally short duration is a teaching/demo choice that makes expiration practical to verify during cross-check.
- **Client Storage Limitation:** The app-session data in `localStorage` is client-controlled and can be read or modified by the user. It is used here to practice persistence across reloads and automatic expiration, not as a security boundary. Do not store passwords, Firebase ID/refresh tokens, or other credentials in this app-session record. The backend does not validate this client-side state.
- **Expiration and Sign-Out:** The active app session is the source of truth for authenticated UI and feature guards. On app-session expiration or explicit logout, clear the app-session data and call Firebase `signOut` so Firebase's own persisted authentication state does not restore the user after the app session has ended.
- **Depends on Story 3:** Routing, URL synchronization, public API data loading, Snackbar, and read-only Game Details/comments from Story 3 are prerequisites. Story 4 extends them with identity and authenticated mutations.

## Common Requirements

Work for this stage should follow the common project rules:

- [MiniGames Common Requirements](common-project-requirements.md)
- [MiniGames Common Scoring Scope: No Pixel Perfect / Layout Match Scoring (Story 3)](tasks/story-3/common-no-pixel-perfect-scoring.md)
- [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](tasks/story-3/common-skeleton-loaders-error-empty-states.md)
- [MiniGames Common Snackbar Notification Requirements (Story 3)](tasks/story-3/common-snackbar-notification-requirements.md)

## Key Resources

- Figma Design: [project](https://www.figma.com/design/4MnLizE59gZI2DDxaSgZqi/MiniGames?node-id=0-1&m=dev&t=fsxihMHW5MYSxEkW-1)

- Project Assets: [folder: tasks/assets](tasks/assets)

- Backend API: [Base URL](https://faxb76kxra.execute-api.eu-central-1.amazonaws.com/api)

- API Endpoint & Schema Specification: [doc URL](https://faxb76kxra.execute-api.eu-central-1.amazonaws.com/docs)

## Authentication & User Registration (140 points)

- (30 points) Real-time validation for Login and Registration forms. [RSS-QS-4-1-1](tasks/story-4/RSS-QS-4-1-1-auth-forms-realtime-validation.md)
- (50 points) Firebase project, Email/Password provider, and SDK setup. [RSS-QS-4-1-3](tasks/story-4/RSS-QS-4-1-3-firebase-auth-setup.md)
- (20 points) Email/Password authentication flow and UI state management. [RSS-QS-4-1-2](tasks/story-4/RSS-QS-4-1-2-auth-registration-api.md)
- (40 points) Google sign-in integration with Firebase Authentication. [RSS-QS-4-1-4](tasks/story-4/RSS-QS-4-1-4-google-oauth.md)

## Authenticated Game Interactions (53 points)

- (15 points) Add to / Remove from Favorites API request. [RSS-QS-4-2-1](tasks/story-4/RSS-QS-4-2-1-favorites-api.md)
- (20 points) Comment submission form with auto-expand textarea & API update. [RSS-QS-4-2-2](tasks/story-4/RSS-QS-4-2-2-comment-submission-form.md)
- (3 points) Comment avatar styling (random token color & initial). [RSS-QS-4-2-3](tasks/story-4/RSS-QS-4-2-3-comment-avatar-styling.md)
- (15 points) Like comment API request. [RSS-QS-4-2-4](tasks/story-4/RSS-QS-4-2-4-like-comment-api.md)

## Authenticated User State, Session & Guards (80 points)

- (30 points) Authenticated user header state, avatar image, and initials calculation. [RSS-QS-4-3-1](tasks/story-4/RSS-QS-4-3-1-authenticated-header-profile.md)
- (20 points) User session persistence in localStorage and 5-minute expiration handling. [RSS-QS-4-3-2](tasks/story-4/RSS-QS-4-3-2-session-persistence-expiration.md)
- (15 points) User logout functionality and guest mode reset. [RSS-QS-4-3-3](tasks/story-4/RSS-QS-4-3-3-logout-guest-mode-reset.md)
- (15 points) Authenticated user Auth dialog URL/UI guard. [RSS-QS-4-3-4](tasks/story-4/RSS-QS-4-3-4-auth-dialog-url-guard.md)

## Unit Testing & Code Coverage (150 points)

- (30 points) Unit Testing Tooling & Packages Installation. [RSS-QS-4-4-1](tasks/story-4/RSS-QS-4-4-1-unit-testing-tooling.md)
- (20 points) Test Execution & Coverage Scripts Setup. [RSS-QS-4-4-2](tasks/story-4/RSS-QS-4-4-2-test-coverage-scripts.md)
- (40 points) Successful Test Execution & Zero Failing Tests. [RSS-QS-4-4-3](tasks/story-4/RSS-QS-4-4-3-successful-test-execution.md)
- (60 points) Code Coverage Target & Genuine Logic Testing. [RSS-QS-4-4-4](tasks/story-4/RSS-QS-4-4-4-code-coverage-target.md)

## Penalties

- **New**: Writing fake or cheating unit tests (e.g., `expect(true).toBe(true)` or dummy calls used solely to artificially inflate code coverage numbers): **-50 points per test**
- **New**: Individual failing unit test assertion: **-10 points per failing test**
- **New**: Total project code coverage (Statements metric `% Stmts`) is between 60% and 79%: **-50 points**
- **New**: Total project code coverage (Statements metric `% Stmts`) is between 40% and 59%: **-70 points**
- **New**: Unit tests are not implemented at all: **-100 points**
- Using standard browser `alert()` or `confirm()` dialogs: **-200 points**
- Client-side filtering, sorting, or pagination applied instead of sending API requests to the backend server: **-200 points**
- The submitted cross-check link is not valid or is not a Pull Request link: **-20 points**
- Changes were made after the deadline: **-40 points**
- Main/base branch is named incorrectly (not following repository workflow guidelines): **-20 points**
- The submitted Cross-Check Pull Request has been merged into the target branch: **-30 points**
- Commits or Pull Request description do not follow the RS School style guide: **-30 points**
- Failure to follow the branching strategy (e.g., implementing all tasks directly in a single branch without separate task branches): **-50 points**
- Prohibited libraries listed in the requirements are used: **-200 points**
- The entire layout or individual layout blocks are implemented using images: **-90 points**
- `console.log` calls are present in the code: **-10 points per unique log, up to -30 points total**
- CSS properties are set with magic values instead of design tokens/constants: **-10 points per unique case, up to -50 points total**
- ESLint or Prettier errors are present in the code: **-5 points per error**
- Presence of explicit `any` type in TypeScript code: **-5 points per occurrence**
