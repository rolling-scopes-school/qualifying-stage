# MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)

These requirements apply to Story 3 tasks that load data from the backend REST API and render data-driven UI sections.

## Skeleton loader

- While an API request is pending, a skeleton-placeholder loading animation should be displayed for the content area being loaded.
- Typical coverage in this story includes: leaderboard table, carousel/slider cards, library game cards list, and game details modal sections.

## Error banner (critical / block-level failures)

- If a primary content-loading API request fails due to a network or server error, an error banner should replace the content area.
- The banner should include a clear error message and a retry control that re-dispatches the failed request.

## Empty data state

- When an API request succeeds but returns no items for the current criteria, show an empty-state placeholder inside the content area.
- Empty-state placeholders must be visually and behaviorally distinct from a network/server error banner.

## Consistent application

- Loading, error, and empty states should be applied consistently across Home, Library, and Game Details data-driven sections implemented in this story.

## Design freedom (not scored for visual match)

- The visual design and layout of skeleton loaders, error banners, and empty-state placeholders are at the student's discretion.
- Implementing them in the overall project style is **recommended**, but reviewers should **not** score whether the look matches project styles, motifs, colors, or Figma visuals.
