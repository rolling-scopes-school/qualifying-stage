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

### [Story 3 — Backend API Integration & Authentication](story-3.md)

Connect the application with the REST API for dynamic data fetching, category filtering, sorting, pagination, skeleton loading, snackbar, and authentication (Email/Password & Firebase Google OAuth).

### [Story 4 — Custom Routing & Unit Testing](story-4.md)

Implement custom SPA routing without external libraries, synchronizing pages, filters, sorting, pagination, and modal dialogs with URL address bar and History API (deep-linking, 404 page, empty data & game-not-found banners). Configure Vitest/Jest unit testing, test scripts, exclusion rationale comments, and achieve code coverage.
