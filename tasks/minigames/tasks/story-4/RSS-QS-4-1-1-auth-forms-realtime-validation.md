# Task RSS-QS-4-1-1: Auth Forms Real-time Validation (30 points)

## Description

Implement real-time client-side validation for Login and Registration forms inside the Auth dialog, with inline error messages and submit-button state management.

## Acceptance Criteria

- **Real-time Validation:** Validation runs as the user types or leaves fields (input/change/blur), not only after submit.
- **Field Rules:** Apply these rules to the active form:
  - **Email (login and registration):** Required; validate that it matches a standard email address format.
  - **Username (registration only):** Required; 2–30 characters long; must start with an uppercase English letter; may contain English letters and digits only.
  - **Password (registration):** Required and at least 6 characters long; must contain at least one uppercase English letter, one digit, and one special character. Passwords may otherwise contain English letters, digits, and special characters.
  - **Confirm password (registration):** Required and must exactly match the password. Validate only the match; do not apply the password rules to this field separately. Revalidate this field whenever the password changes.
  - **Password (login):** Required and at least 6 characters long. Do not apply the registration password-strength rules to login.
- **Inline Error Messages:** Invalid fields show clear inline error messages; valid fields clear those errors.
- **Submit Button State:** Submit remains disabled while the active form is invalid; becomes enabled only when all required fields for the current mode (login/register) are valid.
- **Mode Switch Consistency:** Switching between Login and Registration clears the fields and their validation errors.
