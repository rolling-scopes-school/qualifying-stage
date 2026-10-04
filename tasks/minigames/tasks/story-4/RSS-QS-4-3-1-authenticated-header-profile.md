# Task RSS-QS-4-3-1: Authenticated User Profile Header State (30 points)

## Description

Render the active app-session profile in the site header and mobile menu, using the user's photo when available and initials otherwise.

## Acceptance Criteria

- **Authenticated Header & Mobile Menu UI:** After successful authentication (login or registration), replace the guest controls with the authenticated profile state in the site header and mobile menu according to the mockup.
- **Profile Name:** Display `displayName` as text, never as injected HTML. If it is empty, use the part of `email` before `@`; if that is unavailable, show a generic fallback name.
- **Profile Photo:** If `avatarUrl` is present, render it in the avatar. If it is absent or the image fails to load, show the initials fallback.
- **Initials Fallback:** Trim the selected profile name and split it on whitespace. For one word, show its first alphanumeric character in uppercase; for two or more words, show the first alphanumeric character from each of the first two words in uppercase. Support Unicode letters and digits. If no alphanumeric character is available, show a generic fallback avatar.
