# Task RSS-QS-4-3-3: User Logout Functionality & Guest Mode Reset (15 points)

## Description

Implement user logout functionality via the header and mobile burger menu controls, clearing session data and returning the application to guest mode.

## Acceptance Criteria

- **Logout Controls Availability:** After successful authentication, Logout buttons are accessible in both the main site header and the mobile burger menu (according to the Figma layout).
- **LocalStorage Data Cleanup:** Clicking the Logout button clears user profile and session data stored in `localStorage` (if implemented).
- **Guest Mode Transition:** The application transitions immediately back to unauthenticated guest mode, restoring Login and Registration buttons in the header and mobile menu with full capability to authenticate again.
- **Logout Feedback:** Snackbar displays operation success or failure message with reason.
- **Access Restriction:** Upon logging out, all features restricted to authenticated users (adding games to favorites, submitting comments, liking comments) become inaccessible/restricted according to guest access rules.
