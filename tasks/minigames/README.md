# MiniGames

## Task Goal

Build a web application with 2 pages and 2 dialog windows based on the [design mockup](https://www.figma.com/design/4MnLizE59gZI2DDxaSgZqi/MiniGames?node-id=0-1&m=dev&t=fsxihMHW5MYSxEkW-1):

- Home
- Library
- Auth modal (sign in / sign up)
- Game Details modal (game details)

The project should demonstrate that students can build a full UI using only TS + HTML + SCSS, without frameworks or ready-made UI libraries.

## Key Skills

- Valid semantic responsive web design;
- Easy-to-maintain, readable code;
- Exporting styles and graphics from Figma;
- Using TypeScript to implement the functionality specified in the task.

## Stories

### [Story 1 — Project Setup & Home Page Layout](story-1.md)

Set up the project repository and tooling (bundler, TypeScript, ESLint, Prettier, Husky, Sass tokens), implement the full adaptive layout of the Home page at all three breakpoints, and implement the Auth dialog layout.

### [Story 2 — Library Page Layout, Game Details Dialog & Home Page Slider Logic](story-2.md)

Implement the adaptive layout of the Library page, the Game Details dialog, and the interactive logic of the Home page slider.

### [Story 3 — Backend API Integration & Custom SPA Routing](story-3.md)

Connect the application with the REST API for dynamic public data (Home, Library filter/sort/pagination, Game Details, comments), shared loading/error/empty and Snackbar feedback, and custom SPA routing with URL/History synchronization (deep links, 404 page, empty-data and game-not-found states).

### [Story 4 — Authentication & Unit Testing](story-4.md)

Implement authentication (email/password and Firebase Google OAuth), session-aware UI and guarded dialogs, and authenticated features (favorites, comment submit/like). Configure Vitest/Jest unit testing, test scripts, exclusion rationale comments, and achieve code coverage.
