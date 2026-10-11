.ю5н4е# Alchemist's Cauldron: Common Requirements

These rules are checked together with the story files of this game. If a story gives a more specific rule, follow the story.

## Score

Students can stop after any finished level. Levels are cumulative: Level 2 assumes that Level 1 is fully done, and Level 3 assumes that Level 1 and Level 2 are fully done.

| Level | Points added by this level | Total score |
|---|:---:|:---:|
| 🟣 **Precondition 1** | 58 precondition points | 58 |
| 🟢 **Level 1 — Basic** | 170 story points + 30 common requirements points | 228 |
| 🟡 **Level 2 — Extended** | +50 story points | 278 |
| 🔴 **Level 3 — Full game** | +115 story points | 393 |

The 58 precondition points are counted once before Level 1. The 30 common requirements points are counted once, in Level 1. Maximum possible score: **393**.

## Technical requirements

- The game works in the latest Google Chrome.
- Use **TypeScript**. Do not use frameworks, CSS frameworks, game engines or other libraries.
- Do not use the `any` type.
- Draw icons and shapes with CSS, SVG or text symbols. Do not use pictures or icon fonts for game elements.
- Work in Git with task branches, small step-by-step commits and a public deployed link.
- The game must be usable on screens from **375 px** to **1920 px** wide, without a horizontal page scrollbar.
- There is no ready design file. Pixel-perfect matching is not checked.

## Working with the Repository

The project is split into stories. To keep the review diff focused, follow this branch and Pull Request workflow:

1. **Story 1 (`story-1`):**
   - Create `story-1` from `main` or `master`.
   - For each task, or a small logically related group of tasks, create a feature branch from `story-1`, make the changes, and open a Pull Request back into `story-1`.
   - Merge the task Pull Requests into `story-1`.
   - When Story 1 is complete, create a Pull Request from `story-1` into `main`.
   - Do **not** merge this final Pull Request. Submit its link for Cross-Check.

2. **Story 2 and Story 3:**
   - Create `story-2` from `story-1`, and `story-3` from `story-2`.
   - For each task, or a small logically related group of tasks, create a feature branch from the current story branch, make the changes, and open a Pull Request back into that story branch.
   - Merge the task Pull Requests into the current story branch.
   - When the story is complete, create a Pull Request from `story-2` into `story-1`, or from `story-3` into `story-2`.
   - Do **not** merge this final Pull Request. Submit its link for Cross-Check.

> **Note on task branches:** Small tasks that are closely related by context or logic may be combined in one feature branch.
>
> **Why target the previous story branch?**  
> A Pull Request from `story-N` into `story-(N-1)` contains only the changes made in Story N, so the diff stays clean for reviewers.

## Submitting for Cross-Check

- After finishing the story and creating the final Pull Request, go to the RS App at <https://app.rs.school/>.
- Select **Cross-Check: Submit**, choose the relevant task from the dropdown menu, and paste the unmerged Pull Request link into the **Solution URL** field.
- Click **Submit**.

> **Submission recommendation:** submit as soon as the option is available in RS App. After that, you can keep working until the deadline.

## Rules that stay the same in all stories

- **Timer:** calculate the remaining time from timestamps (`Date.now()`), not by counting ticks.
- **Pause:** the Pause button pauses the game. Pause the game when the browser tab becomes hidden.
- **Save:** use `localStorage`. Broken or missing saved data must never crash the game.
- **Continue Game:** when a valid unfinished save exists, show a **Continue Game** button. It opens the game in **paused** state.
- **Player name:** use **2–15** characters. Allowed: letters, digits, space, `_` and `-`.
- **Leaderboard:** keep Top-10 results. Higher score is better. If scores are equal, the earlier result stays higher. Date format: `DD.MM.YYYY HH:MM`.
- **Dialogs:** do not use the browser `alert()` or `confirm()` dialogs for gameplay or task flows. Use custom in-app dialogs instead.
- **Visual effects:** use CSS animations for visual feedback. Do not use `setInterval` or `setTimeout` for decorative animations.

## Common requirements score (30 points)

- **(10 points) Repository and delivery workflow:** repository setup, story and task branches, step-by-step commits, a working public link, and submission of the unmerged final story PR link in RS App.
- **(10 points) Code quality:** ESLint and Prettier are set up and have no errors; no `console.log`; no `any`; game logic is kept outside files with markup.
- **(10 points) Documentation:** the repository README explains which parts of the game are implemented, how the player interacts with the game, how to run the game.

## Penalties

- Forbidden libraries or frameworks are used: **-200 points**
- The layout or game elements are made with images: **-90 points**
- Changes after the deadline: **-40 points**
- `console.log` in the code: **-10 points per unique log, up to -30 points**
- Explicit `any` in TypeScript: **-5 points per occurrence**
- ESLint or Prettier errors: **-5 points per error**
- Commits or Pull Request text do not follow the RS School style guide: **-30 points**
- The game crashes or loses its state when `localStorage` contains broken data: **-20 points**
- Browser `alert()` or `confirm()` dialogs are used instead of custom in-app dialogs: **-10 points per unique case, up to -30 points**
- A visual effect uses `setInterval` or `setTimeout` where a CSS animation is required: **-10 points per unique case, up to -30 points**