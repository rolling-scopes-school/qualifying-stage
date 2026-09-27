# MiniGames Story 3

Total: **310 points**

## Goal

- Connect the MiniGames web application frontend with the backend REST API to dynamically fetch, display, filter, sort, and paginate public data.
- Apply shared UI feedback patterns (skeleton loaders, error banners, empty data placeholders, and custom Snackbar notifications) across API-driven sections.
- Implement a custom SPA routing system using pure TypeScript with History API integration, deep linking, and URL synchronization for pages, Library filters/sorting/pagination, and dialogs.
- Handle navigation edge cases: dedicated 404 Not Found page, Library "Data Not Found" banner, and "Game Not Found" modal state.
- Load Game Details and latest comments in read-only mode (authenticated mutations are deferred to Story 4).

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

- API Endpoint & Schema Specification: [doc URL](<[PLACEHOLDER_API_SCHEMA_URL](https://faxb76kxra.execute-api.eu-central-1.amazonaws.com/docs)>)

> Note:
>
> - Backend REST API endpoints used in this story are treated as **public read** integrations for Home, Library, Game Details, and comments list.
> - **Authenticated features** (auth, favorites toggle, comment submit/like, authenticated header) are **out of scope for Story 3** and are implemented in Story 4.

## Home Page & API Integration (30 points)

- (15 points) Hero Slider / Carousel API data fetching and rendering. [RSS-QS-3-1-1](tasks/story-3/RSS-QS-3-1-1-hero-carousel-api.md)
- (15 points) Top Players Leaderboard API data fetching and rendering. [RSS-QS-3-1-2](tasks/story-3/RSS-QS-3-1-2-leaderboard-api.md)

## Library Page & API Integration (125 points)

- (15 points) Game cards list API data fetching and rendering. [RSS-QS-3-2-1](tasks/story-3/RSS-QS-3-2-1-library-game-cards-api.md)
- (35 points) Category filtering via API request. [RSS-QS-3-2-2](tasks/story-3/RSS-QS-3-2-2-library-category-filtering-api.md)
- (35 points) Game sorting via API request. [RSS-QS-3-2-3](tasks/story-3/RSS-QS-3-2-3-library-sorting-api.md)
- (40 points) Pagination via API request. [RSS-QS-3-2-4](tasks/story-3/RSS-QS-3-2-4-library-pagination-api.md)

## Game Details Dialog & API Integration (60 points)

- (30 points) Game details data API loading and rendering. [RSS-QS-3-3-1](tasks/story-3/RSS-QS-3-3-1-game-details-api.md)
- (30 points) Game comments fetching. [RSS-QS-3-3-2](tasks/story-3/RSS-QS-3-3-2-game-comments-fetch-api.md)

## Custom SPA Routing & URL Synchronization (95 points)

- (80 points) Custom SPA Routing & URL Synchronization (pages, Library filter/sort/pagination, dialogs; History API, deep links, Single Source of Truth). [RSS-QS-3-4-1](tasks/story-3/RSS-QS-3-4-1-spa-router-url-synchronization.md)
- (15 points) 404 Not Found Page & Invalid Route Handling. [RSS-QS-3-4-2](tasks/story-3/RSS-QS-3-4-2-404-not-found-page.md)

## Penalties

- **New**: Using standard browser `alert()` or `confirm()` dialogs: **-200 points**
- **New**: Client-side filtering, sorting, or pagination applied instead of sending API requests to the backend server: **-200 points**
- The submitted cross-check link is not valid or is not a Pull Request link: **-20 points**
- Changes were made after the deadline: **-40 points**
- Main/base branch is named incorrectly (not following repository workflow guidelines): **-20 points**
- The submitted Cross-Check Pull Request has been merged into the target branch: **-30 points**
- Commits or Pull Request description do not follow the RS School style guide: **-30 points**
- Failure to follow the branching strategy (e.g., implementing all tasks directly in a single branch without separate task branches): **-50 points**
- Prohibited libraries listed in the requirements are used: **-200 points**
- The entire layout or individual layout blocks are implemented using images: **-90 points**
- `console.log` calls are present in the code: **-10 points per unique log, up to -30 points total**
- ESLint or Prettier errors are present in the code: **-5 points per error**
- Presence of explicit `any` type in TypeScript code: **-5 points per occurrence**
