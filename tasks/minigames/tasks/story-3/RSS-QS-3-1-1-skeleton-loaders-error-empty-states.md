# Task RSS-QS-3-1-1: Skeleton Loaders, Error Banners, and Empty States (50 points)

## Description

Implement skeleton loading placeholder animations, network/server error banners, small element error snackbars, and empty state banners for data loaded from the backend API.

## Acceptance Criteria

- **Skeleton Loader:** While an API request is pending, a skeleton-placeholder loading animation should be displayed for the content area being loaded (leaderboard table, carousel/slider cards, library game cards list, game details modal sections).
- **Error Banner (Critical / Block-Level Failures):** If a primary content-loading API request fails due to a network or server error, an error banner should replace the content area. The banner should include a clear error message and a retry control that re-dispatches the failed request.
- **Empty Data State:** When an API request succeeds but returns no items for the current criteria, show an empty-state placeholder inside the content area (distinct from a network error banner).
- **Consistent Application:** Loading, error, and empty states should be applied consistently across Home, Library, and Game Details data-driven sections implemented in this story.
