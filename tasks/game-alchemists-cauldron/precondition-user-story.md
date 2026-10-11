# Story 1 — Project Setup & Technical Base (58 points)

## Goal

Prepare the technical base for Alchemist's Cauldron: repository workflow, code quality tooling, and a predictable project structure before game logic starts.

## Common Requirements

Work for this stage should follow the common project rules:

- [Mini-game Common Requirements](./common-requirements.md)

## Key Resources

- Game README: [README](./README.md)
- Common requirements: [common-requirements](./common-requirements.md)

## Repository Setup (25 points)

- (10 points) [PRE-QS-1-1-1](./tasks/preconditions/precondition-repo-setup-readme.md) Create the game repository, README and .gitignore.
- (10 points) [PRE-QS-1-1-2](./tasks/preconditions/precondition-folder-structure.md) Set up a clear and organized folder structure for the game.
- (5 points) [PRE-QS-1-1-3](./tasks/preconditions/precondition-pull-request-template.md) Create a pull request template with a clear structure.

## Development Environment Configuration (33 points)

- (10 points) [PRE-QS-1-2-1](./tasks/preconditions/precondition-bundler-setup.md) Set up and configure the bundler for development and production builds.
- (5 points) [PRE-QS-1-2-2](./tasks/preconditions/precondition-typescript-config.md) Configure TypeScript for strong typing.
- (5 points) [PRE-QS-1-2-3](./tasks/preconditions/precondition-eslint-setup.md) Set up ESLint for consistent code quality checks.
- (5 points) [PRE-QS-1-2-4](./tasks/preconditions/precondition-prettier-config.md) Configure Prettier for automatic formatting.
- (8 points) [PRE-QS-1-2-5](./tasks/preconditions/precondition-husky-git-hooks.md) Initialize Husky for commit and push hooks.

## Hints

1. Keep game logic outside DOM rendering files from the start.
2. Match folder names to the game domain, for example `data/`, `logic/`, `state/`, `storage/`, `ui/`, `styles/`, and `assets/`.
3. Make sure the tooling works with the code style rules from the common requirements.
4. Keep the setup clean enough that the later story files can focus on gameplay only.
