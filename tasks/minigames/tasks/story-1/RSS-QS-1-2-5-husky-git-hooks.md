# Task RSS-QS-1-2-5: Initialize Husky (8 points)

## Description

Initialize Husky to manage Git hooks, automating commit message validation, code formatting, and linting checks during the Git workflow.

## Acceptance Criteria

- Husky is initialized and integrated into the project.
- A `commit-msg` hook is configured to validate commit messages against the [RS School Git Guideline](https://rs.school/docs/git-convention). Commits with messages that do not follow the convention should be rejected.
- A `pre-push` hook is configured to run ESLint and Prettier checks before pushing code to the remote repository.
- If ESLint or Prettier returns any errors or warnings, `git push` should be aborted.
