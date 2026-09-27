# Task RSS-QS-3-1-2: Snackbar Notification Component (10 points)

## Description

Implement a reusable Snackbar notification component for non-blocking user feedback on success, warning, and error events.

## Acceptance Criteria

- **Reusable Component:** A single Snackbar component/module can be triggered from different parts of the application.
- **Message Variants:** Supports at least success and error (and optionally warning/info) message states with visually distinct styling.
- **Auto-Dismiss:** The Snackbar automatically disappears after a reasonable timeout without blocking page interaction.
- **Manual Dismiss (Optional but Recommended):** User can close the Snackbar manually via a close control if provided by the design.
- **Non-Blocking UI:** Showing a Snackbar must not freeze navigation, scrolling, or other interactive controls.
