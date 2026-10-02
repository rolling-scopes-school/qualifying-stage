# Task RSS-QS-4-2-2: Comment Submission Form & Auto-expand Textarea (20 points)

## Description

Implement the comment submission form inside the Game Details dialog with an auto-expanding textarea, submit via Enter key or button, and API comments list refresh.

## Acceptance Criteria

- **Initial State:** When opening the Game Details dialog, the comment text field is cleared.
- **Auto-Expanding Textarea:** Textarea expands vertically as text is typed according to the design layout. Upon reaching maximum height, an internal vertical scrollbar appears inside the textarea.
- **Submission Trigger:** Comment submission is triggered by clicking the Send button or pressing the `Enter` key (without `Shift`).
- **Input Locking during Request:** While sending the comment API request, the textarea input and submit button are locked (disabled state).
- **Input Sanitization & XSS Protection:** Submitted comment text should be sanitized/escaped to prevent Cross-Site Scripting (XSS) attacks and malicious script/HTML injection before rendering in the DOM.
- **Operation Feedback & Error Recovery:** Snackbar displays operation success or failure message with reason. If the submission request fails or returns an error, the form fields and submit button are unlocked, and the typed comment text SHOULD NOT be cleared from the textarea, allowing the user to retry.
- **Post-Submission Reset:** Upon successful submission, the textarea is cleared, a new API request is dispatched to fetch the updated list of 3 latest comments, and the total comment count in the section header is updated.
- **Access Control:** Comment posting is available ONLY to authenticated users. For guest/unauthenticated users, the comment input block should be locked/disabled or hidden.
- **Authenticated User Avatar in Comment Form:** The comment submission form displays the **uppercase first letter** of the authenticated user's username.
