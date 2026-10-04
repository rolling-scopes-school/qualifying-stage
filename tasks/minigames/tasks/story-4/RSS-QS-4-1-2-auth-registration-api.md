# Task RSS-QS-4-1-2: Authentication & Registration API Requests (20 points)

## Description

Wire Login and Registration form submit actions to authentication requests with pending UI locks, loading feedback, and success/error handling.

## Acceptance Criteria

- **Submit Dispatches Auth Request:** Valid form submission triggers the corresponding login or registration authentication flow.
- **Input Locking during Request:** While the authentication request is pending, form inputs and submit controls are locked (disabled).
- **Dialog Closing Lock during Pending Request:** While the authentication request is pending and inputs are locked, the entire Auth dialog SHOULD NOT be closable by the user.
- **Request Outcome Handling:** On failure, inputs unlock and the user can retry; on success, the dialog closes and the authenticated UI state is applied.

- Loading, error, empty, and Snackbar feedback follow [MiniGames Common Skeleton Loaders, Error Banners, and Empty States (Story 3)](../story-3/common-skeleton-loaders-error-empty-states.md) and [MiniGames Common Snackbar Notification Requirements (Story 3)](../story-3/common-snackbar-notification-requirements.md). This is a mandatory criterion.
