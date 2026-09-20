# MiniGames Common SPA Navigation Requirements (Story 2)

These requirements apply to Story 2 tasks that involve page links and client-side navigation between Home and Library.

## Navigation targets

- In Story 1, application links pointed to the Home page.
- In Story 2, links that represent the Library page should open the Library page.
- Links that represent the Home page should open the Home page.
- Other links that do not correspond to an existing application page in the mockup (for example, social media icons and placeholder/non-existent pages) continue to point to the Home page, as in Story 1.

## Active navigation state

- The navigation item for the currently open page is visually marked as active.
- The active state is shown correctly in both the header and the mobile burger menu.
- The active state updates when the user navigates between the Home and Library pages.

## SPA behavior scope

- Home ↔ Library navigation should work as client-side SPA navigation and should not trigger a full page reload.
- A minimal in-app page switch is enough for Story 2 (for example, rendering the target page via TypeScript).
- Full URL synchronization with the History API, deep-linking, and related routing edge cases are out of scope for Story 2 and will be implemented later.
