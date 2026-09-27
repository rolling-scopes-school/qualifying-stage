# Task RSS-QS-3-4-1: Custom SPA Routing & URL Synchronization (80 points)

## Description

Implement a custom SPA router in pure TypeScript and keep application UI state synchronized with the browser URL and History API.

The same rules apply to **pages**, **Library interactive controls**, and **modal dialogs**:

- **Single Source of Truth with API / UI state:** user actions that change navigable state update the URL; the URL is used to restore UI state and to trigger the matching data loading where applicable.
- **Deep Link State Restoration:** opening a copied URL in a new tab restores the same page, controls, and dialogs.
- **Browser History Controls:** Back / Forward update the URL and restore the corresponding UI state without a full page reload.

## Acceptance Criteria

- **No External Routing Libraries:** routing is implemented in pure TypeScript only. Third-party routers are prohibited.
- **SPA Behavior:** page views switch without full browser reloads.
- **Main Routes:**
  - `/` or `/home` — Home page
  - `/library` — Library page

List of navigable states that **should write to the URL** when changed by the user and **should be restored** (UI + required data fetch) when the URL is opened or reached via history:

| Area    | State                        | Example URL shape                              |
| ------- | ---------------------------- | ---------------------------------------------- |
| Pages   | Active page (Home / Library) | `/`, `/home`, `/library`                       |
| Library | Category filter              | `category=<category-name>`                     |
| Library | Sort order                   | `sort=<sort-field>`                            |
| Library | Pagination page              | `page=<page-number>`                           |
| Dialogs | Game Details open + game id  | `?game=<game-id>` or `/game/<game-id>`         |
| Dialogs | Auth open + mode             | `?auth=login` or `?auth=register` th=register` |

**Full examples:**

- `/library?category=puzzle&sort=rating-desc&page=2`
- `/library?category=arcade&page=2&game=<game-id>`
- `/?auth=login`
- `/library?auth=register`

Exact query key names and path vs query style for game/auth may vary, but the mapping must be consistent, shareable, and history-friendly.

### Single Source of Truth

- Changing any state from the table above updates the address bar without reload.
- Closing a dialog (Close control, backdrop click, Escape) clears or reverts the dialog part of the URL without reload.
- For Library filter / sort / pagination and Game Details, URL-driven state must match the API request parameters and the rendered UI (selected chip, sort value, page, open modal content).

### Deep Link State Restoration

Opening a URL (new tab, paste, bookmark) must restore:

- the correct page view;
- Library: active category chip, selected sort option, current page, and the corresponding games request/result;
- Dialogs: base page under the modal, automatically opened Game Details or Auth dialog; for game URLs — load that game's details.

### Browser History Controls

- Back / Forward must move through page, Library query, and dialog URL changes.
- Back while a dialog is open closes the dialog and restores the underlying page URL/state.
- History navigation must update both the URL and the visible UI (and refetch when Library/game data depends on the restored URL).
