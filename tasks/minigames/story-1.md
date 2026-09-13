# MiniGames Story 1

Total: **294 points**

## Goal

- Set up the project repository, tooling (bundler, TypeScript, ESLint, Prettier, Husky), and Sass design tokens.
- Implement the adaptive layout of the Home page at all three breakpoints.
- Implement the Auth dialog layout.

## Common Requirements

Work for this stage should follow the common project rules:

- [MiniGames Common Requirements](common-project-requirements.md)

## Key Resources

- Figma Design: [project](https://www.figma.com/design/4MnLizE59gZI2DDxaSgZqi/MiniGames?node-id=0-1&m=dev&t=fsxihMHW5MYSxEkW-1)

- Project Assets: [folder: tasks/assets](tasks/assets)

- Mock Data / API: [folder tasks/mock-data](tasks/mock-data)

> **Note on Backend Integration & Mock Data**
>
> - Backend integration is strictly out of scope for this stage and we're not implemented it.
> - The provided mock data is optional and intended solely to ease the eventual transition to the API in future stages. You are welcome to shape your data models around it, but you are **not required** to use it.
> - Please note that the real backend is still under active development, so the final API endpoints and data structure may differ slightly from the current mocks.

## Repository Setup (25 points)

- (10 points) Create a GitHub repository for the project, complete with a README file, .gitignore, and necessary dependencies. [RSS-QS-1-1-1](tasks/story-1/RSS-QS-1-1-1-repo-setup-readme.md)
- (10 points) Set up a clear and organized folder structure within the repository, ensuring a maintainable and scalable codebase. [RSS-QS-1-1-2](tasks/story-1/RSS-QS-1-1-2-folder-structure.md)
- (5 points) Create a pull request template with a clear structure for describing proposed changes and the rationale behind them. [RSS-QS-1-1-3](tasks/story-1/RSS-QS-1-1-3-pull-request-template.md)

## Development Environment Configuration (63 points)

- (10 points) Set up and configure a bundler (e.g., Webpack, Vite, Parcel, or other) for the project, supporting both development and production build modes. [RSS-QS-1-2-1](tasks/story-1/RSS-QS-1-2-1-bundler-setup.md)
- (5 points) Configure TypeScript to enforce strong typing and improve code quality throughout the project. [RSS-QS-1-2-2](tasks/story-1/RSS-QS-1-2-2-typescript-config.md)
- (5 points) Set up ESLint to enforce consistent coding styles and identify potential issues in the codebase. [RSS-QS-1-2-3](tasks/story-1/RSS-QS-1-2-3-eslint-setup.md)
- (5 points) Configure Prettier to automatically format code, ensuring a consistent and readable code style. [RSS-QS-1-2-4](tasks/story-1/RSS-QS-1-2-4-prettier-config.md)
- (8 points) Initialize Husky to manage Git hooks, automating tasks such as code formatting and linting checks during the commit process. [RSS-QS-1-2-5](tasks/story-1/RSS-QS-1-2-5-husky-git-hooks.md)
- (10 points) Add and configure Sass, tokens, breakpoints, and shared style utilities. [RSS-QS-1-2-6](tasks/story-1/RSS-QS-1-2-6-sass-tokens-breakpoints.md)
- (20 points) Implement SPA architecture. [RSS-QS-1-2-7](tasks/story-1/RSS-QS-1-2-7-spa-architecture.md)

## Development Scripts (10 points)

- (5 points) Create a script for running ESLint across the codebase, enabling quick and efficient identification of coding style issues and potential errors. [RSS-QS-1-3-1](tasks/story-1/RSS-QS-1-3-1-eslint-script.md)
- (5 points) Create a script for running Prettier across the codebase, simplifying code formatting and ensuring uniform code style. [RSS-QS-1-3-2](tasks/story-1/RSS-QS-1-3-2-prettier-script.md)

## Adaptive Layout: Home Page (130 points)

- (15 points) Implement the site header for the unauthenticated user state. [RSS-QS-1-4-1](tasks/story-1/RSS-QS-1-4-1-header-unauthenticated.md)
- (25 points) Implement the mobile burger menu (≤ 768px). [RSS-QS-1-4-2](tasks/story-1/RSS-QS-1-4-2-burger-menu-mobile.md)
- (15 points) Implement the Hero section. [RSS-QS-1-4-3](tasks/story-1/RSS-QS-1-4-3-hero-section.md)
- (25 points) Implement the static layout of the Carousel/Slider section. [RSS-QS-1-4-4](tasks/story-1/RSS-QS-1-4-4-carousel-slider.md)
- (15 points) Implement the Leaderboard Table section. [RSS-QS-1-4-5](tasks/story-1/RSS-QS-1-4-5-leaderboard-table.md)
- (15 points) Implement the "Are You a Game Developer?" section. [RSS-QS-1-4-6](tasks/story-1/RSS-QS-1-4-6-game-dev-section.md)
- (20 points) Implement the Footer. [RSS-QS-1-4-7](tasks/story-1/RSS-QS-1-4-7-footer.md)

## Auth Dialog Layout (50 points)

- (10 points) Auth dialog trigger, position, and backdrop. [RSS-QS-1-5-1](tasks/story-1/RSS-QS-1-5-1-auth-dialog-trigger.md)
- (10 points) Auth dialog open/close animations and dismiss behavior. [RSS-QS-1-5-2](tasks/story-1/RSS-QS-1-5-2-auth-dialog-animations.md)
- (10 points) Login/Registration switcher and block transitions. [RSS-QS-1-5-3](tasks/story-1/RSS-QS-1-5-3-auth-login-register-switcher.md)
- (10 points) Semantic form markup and input types. [RSS-QS-1-5-4](tasks/story-1/RSS-QS-1-5-4-auth-form-semantic-markup.md)
- (10 points) Responsive visual quality and UI states. [RSS-QS-1-5-5](tasks/story-1/RSS-QS-1-5-5-auth-responsive-ui-states.md)

## Global Layout Verification (16 points)

- (12 points) Global semantic/layout validation. [RSS-QS-1-6-1](tasks/story-1/RSS-QS-1-6-1-global-semantic-validation.md)
- (4 points) Favicon is added to the implemented page in this story.

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
- ESLint or Prettier errors are present in the code: **-5 points per error**
- Presence of explicit `any` type in TypeScript code: **-5 points per occurrence**
