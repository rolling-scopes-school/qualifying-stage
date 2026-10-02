# Task RSS-QS-4-1-2: Authentication & Registration API Requests (20 points)

## Description

Wire Login and Registration form submit actions to authentication requests with pending UI locks, loading feedback, and success/error handling.

## Acceptance Criteria

- **Submit Dispatches Auth Request:** Valid form submission triggers the corresponding login or registration authentication flow.
- **Input Locking during Request:** While the authentication request is pending, form inputs and submit controls are locked (disabled).
- **Dialog Closing Lock during Pending Request:** While the authentication request is pending and inputs are locked, the entire Auth dialog SHOULD NOT be closable by the user.
- **Loading Animation:** A loading animation/spinner signals that the authentication request is being processed.
- **Success & Error Feedback:** Success and failure are communicated via Snackbar (or equivalent non-`alert()` feedback). On failure, inputs unlock and the user can retry; on success, the dialog closes and the authenticated UI state is applied.
