# Task RSS-QS-4-4-4: Code Coverage Target & Genuine Logic Testing (60 points)

## Description

Achieve 80%+ code coverage on the `% Stmts` metric across application logic files and ensure unit tests genuinely evaluate application business logic without artificial/fake test shortcuts.

## Acceptance Criteria

- **Statements Coverage Metric (`% Stmts`):** Running the coverage script should generate a coverage table where total project statement coverage (checked via the first column **`% Stmts`** in the Vitest/Jest terminal coverage table) reaches **80% or higher**.
- **Genuine Logic Verification:** Tests should actively validate actual application code, logic branches, state updates, validation functions, session/auth helpers, API query builders, and router behavior.
- **Prohibition of Fake / Cheating Tests:** Writing superficial or cheating tests (e.g., dummy tests with `expect(true).toBe(true)` or empty render calls written solely to artificially boost coverage percentages) is strictly forbidden.
