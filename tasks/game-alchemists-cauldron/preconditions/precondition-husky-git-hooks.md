# Task PRE-QS-1-2-5: Initialize Husky (8 points)

## Description

Initialize Husky to manage Git hooks for Alchemist's Cauldron and automate commit message validation, formatting, and lint checks during the Git workflow.

## Acceptance Criteria

- Husky is initialized and integrated into the project.
- A `commit-msg` hook validates commit messages against the RS School Git guideline.
- A `pre-push` hook runs ESLint and Prettier checks before pushing code.
- If lint or formatting checks fail, the push is blocked.

## Useful Links

- [Husky](https://typicode.github.io/husky/)
