# Task RSS-QS-3-3-3: Library Pagination via API (30 points)

## Description

Implement Library pagination through backend API page/limit parameters and update pagination controls from response metadata.

## Acceptance Criteria

- **Server-Side Pagination:** Changing page dispatches a backend API request with the selected page (and limit if required by the API).
- **Controls from Metadata:** Pagination UI (current page, total pages, disabled prev/next states) is driven by API response metadata (`totalPages` / equivalent), not by guessing on the client.
- **Results Update:** The game cards list shows only the items returned for the requested page.
- **Reset Behavior:** Changing category filter or sort should reset pagination to page 1 and request the first page from the API.
- **Loading & Error Handling:** Page changes show loading state; failures provide error feedback.
- **No Client-Side-Only Pagination Penalty Path:** Pagination must not be implemented solely by slicing a full client-side list when the API supports page parameters.
