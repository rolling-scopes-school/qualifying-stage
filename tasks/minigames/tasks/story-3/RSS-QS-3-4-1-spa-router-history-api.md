# Task RSS-QS-3-4-1: Custom SPA Router Core & History API Navigation (40 points)

## Description

Implement a custom Single Page Application (SPA) router using pure TypeScript without third-party routing libraries, with full support for browser History API navigation (`pushState`, `replaceState`, `popstate`).

## Acceptance Criteria

- **No External Routing Libraries:** The routing system should be built entirely with pure TypeScript. Using third-party router libraries is strictly prohibited.
- **SPA Behavior & Dynamic View Rendering:** Page view components (Home, Library) switch dynamically on the fly without triggering full browser page reloads.
- **Main Route Definitions:** Support main application routes:
  - `/` or `/home`: Home page view.
  - `/library`: Library page view.
- **History API Integration:** All route transitions utilize standard browser History API methods (`history.pushState`, `history.replaceState`) and attach an event listener for `window` `popstate`.
- **Browser History Controls (Back / Forward):** Standard browser Back and Forward navigation buttons work correctly, updating both the rendered page view and the URL address bar seamlessly.
- **Header & Navigation Controls:** Clicking the site logo, Header navigation links (Home, Library), or CTA buttons changes the URL address bar and updates the active page view without page reload.
