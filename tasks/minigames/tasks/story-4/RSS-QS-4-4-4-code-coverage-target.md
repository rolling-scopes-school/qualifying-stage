# Task RSS-QS-4-4-4: Code Coverage Target & Genuine Logic Testing (60 points)

## Description

Write meaningful unit tests for application logic and achieve at least 80% statement coverage (`% Stmts`) across all application-logic files included in the coverage report. This is an aggregate project metric, not an 80% requirement for every individual file. Exclude only files without application logic, with each exclusion justified as described in [RSS-QS-4-4-2](RSS-QS-4-4-2-test-coverage-scripts.md).

## Acceptance Criteria

- **Statements Coverage Metric (`% Stmts`):** The coverage script must generate a table whose aggregate `% Stmts` value for the included application-logic files is **80% or higher**. Use the reported value without rounding it up to meet the threshold.
- **Genuine Logic Verification:** Tests must assert observable behavior in application code. Relevant targets include form validation; app-session creation, reload validation, expiration and logout; auth-dialog guards; favorite, comment submission and comment-like request/state handling; and API query construction or routing logic where implemented. Include meaningful success and failure cases for asynchronous mutations.
- **External Services:** Tests do not need live Firebase credentials or backend access. Stub or mock Firebase and network boundaries, then assert that the application invokes them correctly and updates its state for success and failure responses.
- **Prohibition of Fake / Cheating Tests:** Tests that do not verify application behavior, such as `expect(true).toBe(true)` or empty render calls used solely to inflate coverage, do not count toward this criterion and are prohibited.
