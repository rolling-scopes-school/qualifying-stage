# Task RSS-QS-4-3-1: Authenticated User Profile Header State (30 points)

## Description

Update the site header UI state for authenticated users, rendering user profile name and Google avatar image or custom initials avatar.

## Acceptance Criteria

- **Authenticated Header & Mobile Menu UI:** After successful authentication (login or registration), the site header and mobile burger menu update according to the authenticated mockup state.
- **Auth & Logout Controls:** Login and Registration buttons are no longer rendered; the Logout button becomes visible and operational in both the main header and mobile burger menu.
- **Username Display & XSS Protection:** Displays the user's profile name in the header block. User display names should be sanitized/escaped to prevent XSS attacks.
- **Google OAuth Avatar:** If the user authenticated via a Google account and the auth response contains a Google avatar photo URL, render the photo in the header avatar container.
- **Initials Avatar Fallback:** If no photo URL exists (or user logged in via Email/Password):
  - Whitespace should be trimmed (`.trim()`) and split by whitespace (`/\s+/`).
  - Single-word name: avatar displays 1 uppercase initial inside (e.g. `Alex` -> `A`).
  - Multi-word name (2+ words): avatar displays 2 uppercase initials composed of the first letters of the first two words (e.g. `John Doe Smith` -> `JD`).
  - Non-alphabetic names: If the display name begins with non-alphabetic characters (e.g. Google profile names like `@user`), use the first available alphanumeric uppercase character.
