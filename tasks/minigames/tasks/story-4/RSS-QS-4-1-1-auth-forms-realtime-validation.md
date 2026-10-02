# Task RSS-QS-4-1-1: Auth Forms Real-time Validation (30 points)

## Description

Implement real-time client-side validation for Login and Registration forms inside the Auth dialog, with inline error messages and submit-button state management.

## Acceptance Criteria

- **Real-time Validation:** Validation runs as the user types or leaves fields (input/change/blur), not only after submit.
- **Field Rules:** Enforce the project validation rules for email/username and password (and password confirm on registration if required by the form design).
- **Inline Error Messages:** Invalid fields show clear inline error messages; valid fields clear those errors.
- **Submit Button State:** Submit remains disabled while the active form is invalid; becomes enabled only when all required fields for the current mode (login/register) are valid.
- **Mode Switch Consistency:** Switching between Login and Registration resets or revalidates fields according to the active form mode without stale errors from the other mode.
