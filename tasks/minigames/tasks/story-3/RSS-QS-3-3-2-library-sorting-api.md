# Task RSS-QS-3-3-2: Library Game Sorting via API (30 points)

## Description

Implement Library sorting by sending sort parameters to the backend API.

## Acceptance Criteria

- **Server-Side Sorting:** Changing the sort control dispatches a backend API request with the selected sort parameter.
- **UI Sync:** The sort dropdown/control reflects the active sort option.
- **Results Update:** The game cards list order updates according to the API response.
- **Combination with Filters:** Sort works together with the active category filter (both parameters are sent in the same or coordinated API requests).
- **Loading & Error Handling:** Loading and error/empty feedback follow the global UI feedback rules.
- **No Client-Side-Only Sorting Penalty Path:** Sorting must not be implemented solely by sorting a full client-side array when the API supports sort query parameters.
