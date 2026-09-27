# Task RSS-QS-3-3-1: Library Category Filtering via API (30 points)

## Description

Implement Library category filtering by sending filter criteria to the backend API (no client-side-only filtering of a full preloaded list as the primary mechanism).

## Acceptance Criteria

- **Server-Side Filtering:** Changing the active category dispatches a backend API request with the selected category parameter.
- **UI Sync:** The active category chip/control visually reflects the selected filter.
- **Results Update:** The game cards list updates according to the API response for the selected category.
- **Loading & Error Handling:** Pending requests show skeleton/loading state; failures show error feedback with retry capability where applicable.
- **Default State:** An "All Games" (or equivalent default) category requests the unfiltered/default games list from the API.
- **No Client-Side-Only Filtering Penalty Path:** Filtering must not be implemented solely by filtering a once-fetched full dataset on the client when the API supports category query parameters.
