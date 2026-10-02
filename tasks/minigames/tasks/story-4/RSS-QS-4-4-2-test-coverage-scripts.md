# Task RSS-QS-4-4-2: Test Execution & Coverage Scripts Setup (20 points)

## Description

Configure scripts in `package.json` for running project unit tests and generating coverage reports, and configure coverage exclusion rules with mandatory inline comments.

## Acceptance Criteria

- **NPM Execution Scripts:** Include the following scripts in `package.json`:
  - `npm run test` (or `npm test`): runs all unit test suites across the codebase.
  - `npm run test:coverage` (or `npm run coverage`): executes test suites and generates a terminal coverage summary table.
- **Coverage Exclusions & Mandatory Explanatory Comments:**
  - Non-logic setup/config files (e.g. `vite.config.ts`, `.eslintrc`, `tsconfig.json`) and pure entry launcher files without business logic (e.g. root application bootstrap file `app.ts`) may be excluded from coverage calculation.
  - **CRITICAL REQUIREMENT:** EVERY file or path pattern added to coverage exclusion settings SHOULD be accompanied by an inline comment in the configuration file explaining *why* it was excluded.
- **Reviewer Coverage Inspection:** During evaluation, reviewers should inspect the configuration file and terminal coverage table to confirm that all files containing business logic are included and exclusions are explicitly commented.
