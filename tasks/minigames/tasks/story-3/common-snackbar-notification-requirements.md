# MiniGames Common Snackbar Notification Requirements (Story 3)

These requirements apply to Story 3 tasks that need non-blocking user feedback for API-related success, warning, or error events.

## Reusable component

- A single Snackbar component/module can be triggered from different parts of the application.

## Message variants

- Supports at least success and error message states with visually distinct styling.
- Warning and/or info variants are optional but recommended.

## Auto-dismiss

- The Snackbar automatically disappears after a reasonable timeout without blocking page interaction.

## Manual dismiss

- Manual close via a close control is optional but recommended.

## Non-blocking UI

- Showing a Snackbar must not freeze navigation, scrolling, or other interactive controls.
- Standard browser `alert()` / `confirm()` dialogs **should not** be used for this feedback.
