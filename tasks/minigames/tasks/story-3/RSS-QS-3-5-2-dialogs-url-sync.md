# Task RSS-QS-3-5-2: Dialog Windows URL Synchronization & Game Not Found Modal State (40 points)

## Description

Synchronize modal dialog states (Game Details modal, Auth modal) with URL address bar parameters, support deep-link modal auto-opening and browser Back button modal dismissal, and handle invalid game ID errors with a dedicated "Game Not Found" modal state.

## Acceptance Criteria

- **Dialog URL Parameter Sync:** Opening a dialog window updates the browser address bar URL without reloading:
  - Game Details modal: reflects game identifier (e.g., `?game=<game-id>` or `/game/<game-id>`).
  - Auth modal: reflects authentication action (e.g., `?auth=login` or `?auth=register`).
- **Modal Dismissal URL Restoration:** Closing a dialog modal (via Close icon button, backdrop click, or Escape key) reverts or clears the modal parameter from the address bar URL without page reload.
- **Browser Back Button Dismissal:** Pressing the browser Back navigation button while a dialog modal is open closes the modal dialog and reverts the address bar URL to the underlying page state.
- **Deep Link Modal Restoration:** Opening a URL containing a modal parameter in a new tab or window renders the underlying base page and automatically opens the target modal dialog window (fetching game details for game URLs).
- **"Game Not Found" Modal State:** If an invalid game parameter (e.g. invalid/non-existent game ID) is present in the URL or if the backend API returns an error / empty response when loading game details:
  - The Game Details modal displays a dedicated error view inside the dialog body informing the user that the requested game was not found.
  - *The visual design and layout of the "Game Not Found" dialog state are at the student's discretion.*

> **Note:** Authenticated-user Auth dialog guard (block `?auth=` when a session is active) is implemented in Story 4 together with session management.
