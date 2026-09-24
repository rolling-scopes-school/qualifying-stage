# MiniGames Story 2

Total: **257 points**

## Goal

- Implement the Library page and its adaptive layout.
- Implement the Game Details dialog layout.
- Implement the Home page slider interaction logic.
- Pass global semantic/layout verification for Story 2 states.

## Common Requirements

Work for this stage should follow the common project rules:

- [MiniGames Common Requirements](common-project-requirements.md)
- [MiniGames Common SPA Navigation Requirements (Story 2)](tasks/story-2/common-spa-navigation-requirements.md)
- [MiniGames Common Game Details Content Requirements (Story 2)](tasks/story-2/common-game-details-content-requirements.md)

## Key Resources

- Figma Design: [project](https://www.figma.com/design/4MnLizE59gZI2DDxaSgZqi/MiniGames?node-id=0-1&m=dev&t=fsxihMHW5MYSxEkW-1)

- Project Assets: [folder: tasks/assets](tasks/assets)

- Mock Data / API: [folder tasks/mock-data](tasks/mock-data)

> **Note on Emojis vs Icons**
>
> - Emojis in Figma render in Apple style; on Windows (for example in Chrome) they may look different.
> - Using native platform emojis instead of exact icon images is **allowed**.
> - Visual differences caused by native emoji rendering must **not** affect the score.

> **Note on Backend Integration & Mock Data**
>
> - Backend integration is strictly out of scope for this stage and it is not implemented.
> - The provided mock data is optional and intended solely to ease the eventual transition to the API in future stages. You are welcome to shape your data models around it, but you are **not required** to use it.
> - Please note that the real backend is still under active development, so the final API endpoints and data structure may differ slightly from the current mocks.

## Adaptive Layout: Library Page (95 points)

- (5 points) Implement the site header for the unauthenticated user state. [RSS-QS-2-1-1](tasks/story-2/RSS-QS-2-1-1-library-header-unauthenticated.md)
- (5 points) Implement the mobile burger menu (≤ 768px). [RSS-QS-2-1-2](tasks/story-2/RSS-QS-2-1-2-library-burger-menu.md)
- (5 points) Implement the Footer. [RSS-QS-2-1-3](tasks/story-2/RSS-QS-2-1-3-library-footer.md)
- (25 points) Implement the section with title, filtering, and sorting. [RSS-QS-2-1-4](tasks/story-2/RSS-QS-2-1-4-library-filtering-sorting.md)
- (40 points) Implement the section with the list of game cards. [RSS-QS-2-1-5](tasks/story-2/RSS-QS-2-1-5-library-game-cards-list.md)
- (15 points) Implement the pagination section layout. [RSS-QS-2-1-6](tasks/story-2/RSS-QS-2-1-6-library-pagination.md)

## Game Details Dialog Layout (70 points)

- (10 points) Game Details dialog trigger, position, and backdrop. [RSS-QS-2-2-1](tasks/story-2/RSS-QS-2-2-1-game-details-trigger.md)
- (10 points) Game Details dialog open/close animations and dismiss behavior. [RSS-QS-2-2-2](tasks/story-2/RSS-QS-2-2-2-game-details-animations.md)
- (10 points) Hero section with close button. [RSS-QS-2-2-3](tasks/story-2/RSS-QS-2-2-3-game-details-hero-section.md)
- (15 points) Game info section (title, description, badges, Play Now, Add to Favorites). [RSS-QS-2-2-4](tasks/story-2/RSS-QS-2-2-4-game-details-info-section.md)
- (10 points) Top Records section. [RSS-QS-2-2-5](tasks/story-2/RSS-QS-2-2-5-game-details-top-records.md)
- (15 points) Comments section (form, textarea auto-grow, comment list, like buttons). [RSS-QS-2-2-6](tasks/story-2/RSS-QS-2-2-6-game-details-comments.md)

## Home Page Slider Logic (80 points)

- (80 points) Implement the interaction logic of the Home page slider. [RSS-QS-2-3-1](tasks/story-2/RSS-QS-2-3-1-home-slider-interaction-logic.md)

## Global Layout Verification (12 points)

- (12 points) Global semantic/layout validation. [RSS-QS-2-4-1](tasks/story-2/RSS-QS-2-4-1-global-semantic-validation.md)

## Penalties

- The submitted cross-check link is not valid or is not a Pull Request link: **-20 points**
- Changes were made after the deadline: **-40 points**
- Main/base branch is named incorrectly (not following repository workflow guidelines): **-20 points**
- The submitted Cross-Check Pull Request has been merged into the target branch: **-30 points**
- Failure to follow the branching strategy (e.g., implementing all tasks directly in a single branch without separate task branches): **-50 points**
- Prohibited libraries listed in the requirements are used: **-200 points**
- The entire layout or individual layout blocks are implemented using images: **-90 points**
- `console.log` calls are present in the code: **-10 points per unique log, up to -30 points total**
- Commits or Pull Request description do not follow the RS School style guide: **-30 points**
- CSS properties are set with magic values instead of design tokens/constants: **-10 points per unique case, up to -50 points total**
  > **Author note — scoring scope for magic values**
  >
  > Points may be deducted **only** for magic values in the token groups from the design-token requirements:
  > **colors**, **sizes** (including **height** and **width**), **shadows**, **corner radii**, **button sizes**, **font families**, **font sizes**, **font weights**, and **breakpoints**.
  >
  > For any other CSS properties tokens are **recommended** but **not required**. Reviewers must **not** reduce the score for magic values outside the list above.
- ESLint or Prettier errors are present in the code: **-5 points per error**
- Presence of explicit `any` type in TypeScript code: **-5 points per occurrence**
