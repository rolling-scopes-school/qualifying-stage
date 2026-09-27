# Task RSS-QS-3-4-2: 404 Not Found Page & Invalid Route Handling (30 points)

## Description

Implement invalid route handling and a dedicated 404 Not Found page view for unrecognized URL paths, complete with standard Header, Footer, error message, and a button to return to the Home page.

## Acceptance Criteria

- **Invalid Route Handling:** Navigating to an unrecognized or non-existent URL path (e.g., `/unknown`, `/invalid-route`, `/page/abc`) automatically triggers redirection to or rendering of the 404 Not Found page view.
- **Header & Footer Integration:** The 404 page view retains the standard site Header (with navigation menu) and site Footer components.
- **404 Message Body:** The main content section of the 404 page displays a clear error message informing the user that the requested URL does not exist. _The visual layout and styling of the 404 body message are at the student's discretion._
- **Return to Home Action:** The 404 page body includes a prominent button (e.g., "Return to Home Page") that redirects the user back to the Home page (`/` or `/home`) via SPA navigation without page reload.
- **Deep Link Resiliency:** Entering an invalid URL directly into a new browser tab or copying/pasting an invalid route opens the application smoothly in the 404 view without throwing uncaught runtime exceptions.
