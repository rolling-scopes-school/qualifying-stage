# Task RSS-QS-1-2-6: Add and Configure Sass, Tokens, and Shared Style Utilities (10 points)

## Description

Add Sass to the project and organize shared style resources for the design system.
This task covers token storage, breakpoints, and reusable Sass helpers that will be used across the project.

> In this context, a **token** refers to a constant used to define CSS properties, such as sizing, color, typography styles, shadows, and similar attributes.

## Acceptance Criteria

- Sass is added to the project and configured for use in the build.
- A dedicated constants/tokens file is created and used to store layout tokens from the style guide where applicable.
- The following token groups are centralized in the project where relevant: colors, sizes, shadows, corner radii, button sizes, font families, font sizes, and font weights.
- Breakpoints are stored in the constants file and reused throughout the codebase for media queries.
- Sass functions and mixins are stored in separate files and grouped with the shared styling utilities.
- Magic values are avoided for properties that can be represented by tokens.
- If a precise Pixel Perfect adjustment cannot be achieved with existing tokens, manual values may be used together with a student comment explaining why the token-based approach was not enough.
- Any other use of magic values is grounds for score reduction.
- Token naming may be adjusted by the student if needed, but the design system intent should remain clear.
- Not all style guide variables should be migrated, but the project should use tokens whenever possible.
- Example of a small Pixel Perfect adjustment: if a standard token defines `8px`, a student may use `calc(var(--size-1) + 3px)` or an equivalent Sass calculation to reach the required layout size.
