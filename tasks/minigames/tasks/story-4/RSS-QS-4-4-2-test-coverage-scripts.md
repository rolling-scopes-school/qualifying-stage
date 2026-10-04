# Task RSS-QS-4-4-2: Test Execution & Coverage Scripts Setup (20 points)

## Description

Configure scripts in `package.json` for running project unit tests and generating coverage reports. The coverage report must include all application files containing logic; exclusions are allowed only for files that contain no application logic and must have a clear rationale in the test configuration.

## Acceptance Criteria

- **NPM Execution Scripts:** Include the following scripts in `package.json`:
  - `npm run test` (or `npm test`): runs all unit test suites across the codebase.
  - `npm run test:coverage` (or `npm run coverage`): executes test suites and generates a terminal coverage summary table.
- **Coverage Scope & Exclusions:** Include every application file containing logic in the coverage report. Test-framework/configuration files and pure bootstrap files with no application logic may be excluded. Do not exclude files merely because they are difficult to test.
- **Exclusion Rationale:** Add a concise comment next to every excluded file or pattern explaining why it contains no application logic. Use a JavaScript or TypeScript test configuration file when comments are needed; JSON configuration files cannot contain comments.
- **Reviewer Coverage Inspection:** During evaluation, reviewers should inspect the test configuration and terminal coverage table to confirm that application-logic files are included and every exclusion is explained.
