# MiniGames Common Requirements

## Technical Requirements

- The application is displayed correctly and functions properly in the latest version of Google Chrome.
- Using `TypeScript` **is required**.
- Using CSS frameworks (e.g., `Bootstrap`, `Tailwind`) **is not allowed**.
- Using JS frameworks (e.g., `Angular`, `React`, `Vue`, etc.) **is not allowed**.
- Using outdated libraries (e.g. `JQuery`, etc.) or pre-built libraries (e.g. `Swiper`, etc) to implement functionality **is not allowed**.
- Using a style reset with `reset.css` **is not recommended**.
- Adding layout as an image by taking a screenshot of a part of the layout and pasting it into the markup **is not allowed**. Please use tags and characters for layout, and use images only for adding pictures and icons, not for layout elements (buttons, blocks, sections).
- The code should be readable, without minification or obfuscation.

## Work with figma design

Start the task by creating your own copy of the layout. To do this:

- Log in to [Figma](https://www.figma.com/);
- Open the layout;
- On the top panel, click on the arrow next to the layout name, and select the option "Duplicate to your drafts";
- At the top left, open the settings, and choose "Back to files";
- Open the copy of the layout with the label "In Drafts".

## Working with the Repository

The project is divided into separate stories (stages). To ensure that cross-check reviewers see only the changes relevant to the current stage, follow this branch and Pull Request workflow:

1. **First Story (`story-1`):**
   - Create a base branch `story-1` from `main` (or `master`).
   - For each individual task (or small, logically related group of tasks), create a feature branch from `story-1`, make the changes, and create a Pull Request to merge into `story-1`.
   - **Merge** task Pull Requests into `story-1`.
   - Once all tasks for Story 1 are complete, create a Pull Request from `story-1` into `main`.
   - **DO NOT merge** this final Pull Request (`story-1` → `main`). Submit its link for Cross-Check review.

2. **Subsequent Stories (`story-N`, e.g., `story-2`, `story-3`, `story-4`):**
   - Create the story base branch `story-N` from the previous story branch `story-(N-1)`.
   - For each individual task (or small, logically related group of tasks), create a feature branch from `story-N`, make the changes, and create a Pull Request to merge into `story-N`.
   - **Merge** task Pull Requests into `story-N`.
   - Once all tasks for Story N are complete, create a Pull Request from `story-N` into `story-(N-1)`.
   - **DO NOT merge** this final Pull Request (`story-N` → `story-(N-1)`). Submit its link for Cross-Check review.

> **Note on Task Branches:** Small tasks that are closely related by context or logic may be combined and implemented in a single feature branch.  
> **Why target `story-(N-1)`?**  
> A Pull Request from `story-N` into `story-(N-1)` contains **only the changes made during Story N**, keeping the diff clean and focused for reviewers.

**Submitting for Cross-Check:**

- After completing the story and creating the final Pull Request, go to the RS App at <https://app.rs.school/>.
- Select **Cross-Check: Submit**, choose the relevant task from the dropdown menu, and add the unmerged **Pull Request link** in the **Solution URL** field.
  elect **Cross-Check: Submit**, choose the relevant task from the dropdown menu, and add the unmerged **Pull Request link** in the **Solution URL** field.
- Click the **Submit** button.

> **Submission Recommendations**
>
> - It is recommended to submit the task as early as possible, as soon as the option becomes available in the RS App. After submission, you can continue working on the task until the deadline.
> - Make sure the deployed link you provide opens in the browser's incognito mode.

## Commit Requirements

- Commits should show your step-by-step personal development history for each task.
- [Use commit names according to the guideline](https://rs.school/docs/git-convention).

> [!CAUTION]
> **CRITICAL REQUIREMENT:** Commits should demonstrate your personal, step-by-step development process. Implementing a large or complex task in only 1–2 bulk commits is strictly forbidden and constitutes grounds for **expulsion from the course by course administrators**.

## Deployment

The project **should be deployed** and accessible via a public link.  
You may use **any deployment platform** of your choice, for example:

- GitHub Pages
- Vercel
- Netlify
- or any other suitable hosting service

The choice of deployment tool does not affect the evaluation, as long as the deployed version of the project is available and works correctly.

## Layout Verification with Pixel Perfect

- Deviation from the mockup of up to **10px** horizontally and vertically is allowed, provided that the overall visual similarity between the layout and the design is maintained.
- Use the [PerfectPixel](https://chrome.google.com/webstore/detail/perfectpixel-by-welldonec/dkaagdgjmgdmbnecmcefdhjekcoceebi?hl=ru) browser extension to compare the layout against the Figma design.
- When checking with PerfectPixel, make sure the extension is set to scale **1**, and both the browser and OS are set to **100% zoom**.
- The target breakpoints for Pixel Perfect verification are **375px**, **768px**, and **1920px**. Each block and section is reviewed independently — shortcomings in one block do not carry over to the next.
- Regarding text: check alignment and spacing relative to the block boundaries. Text height is checked; deviations in word width or letter spacing are not considered errors if the correct font and its specified properties are used.
- If the screen resolution exceeds 1920px, center the layout horizontally or align it manually with the top-left corner guides for comparison.
- If the screen resolution is 1920px or less, use the Device Toolbar in Google Chrome in Responsive mode.
- When verifying at 1920px width, the layout may compress by approximately 17px due to the browser scrollbar consuming part of the viewport. This is expected behavior.

## Responsive Behavior Check in DevTools

1. **Open DevTools:**
   - Press `F12` (Windows/Linux) or `Cmd+Option+I` (Mac), or right-click the page and choose **Inspect**.
   - Click the **Toggle device toolbar** icon in the top-right corner of the DevTools panel.
   - Select **Responsive** in the top panel.

2. **Remove the vertical scrollbar in Responsive mode** (if present):
   - Switch the device type from `Desktop` to `Mobile` in the Device Toolbar.
   - If the device type selector is not visible, click the three dots on the right side of the toolbar and select **Add device type**.

3. Set the screen width to each target breakpoint (375, 768, 1920) and verify that the layout matches the Figma design at each point.

4. **Check fluid resizing:** smoothly drag the screen width from the maximum (1920px) down to the minimum (375px) and confirm that no horizontal scrollbar appears at any width. If a scrollbar or a white gap appears on the right, try refreshing the page.

5. **Zoom tolerance:** when the browser or OS zoom level is not exactly 100%, the reported width may differ by 1–2px (e.g., DevTools shows 768px but the actual value is 767 or 769). Adjust the breakpoint transition point accordingly.

6. **Hover state check on mobile:** in `Mobile` device type, click an interactive element and confirm it does not stay in a hover state. Switch to `Desktop` device type to verify hover effects are active.
