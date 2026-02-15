# Online ZOO

# Project description

Online Zoo is a virtual platform that allows users to observe animals living in zoos or in the wild through live-streaming cameras installed in their habitats.

Users can select an animal in several ways: from the main landing page, via an interactive map, or using a menu with animal icons on the live streaming page.

The project includes an interactive Feed the Animal feature. When the user clicks the FEED button, a popup window opens, visually simulating the feeding process. After the required payment fields are filled in, food is delivered to the animal’s enclosure.

No real payment or transaction system is implemented. However, the entire visual flow and user interaction should be fully implemented according to the provided design.

The Online Zoo project focuses on building a **responsive multi-page website**, implementing layouts, popups, and interactive elements to enhance user engagement. It is designed to help you demonstrate your **front-end development skills** while applying responsive design principles and working with user interface interactions.

The duration of the task is **two weeks**.  
The assignment is evaluated through a **cross-check review** process.

# Project Structure & Design Requirements

## Pages Included in the Design

**The Figma layout contains 4 pages:**

- Landing page _(main page)_
- Map page
- Animal page _(4 different animals implemented using the same layout template)_
- Contact / Feedback page

## Pop-up Windows

**The design includes 2 modal windows:**

- Together we care, save and protect!
- Make your donation

## Supported Screen Widths

**The project should be responsive and support the following screen widths:**

- 1920px
- 1200px
- 640px
- 320px

# Preparation Before Starting the Task

The assignment should be completed according to the author’s design by Dinky:
[Figma mockup](https://www.figma.com/file/lnK11foY8Aoa6oOlDXovVN/Online-ZOO-Project?node-id=0%3A1)

**The first step is to duplicate the design in Figma**

To duplicate the design in Figma:

1. Open the Figma file using the provided link
2. Click on the file name at the top right corner of the screen
3. From the dropdown menu, select **Duplicate to your drafts**

This will create a local copy of the design that you can use for development.

# Repository Requirements

The assignment should be completed in your **own private repository**.  
During development, the repository **should remain private** to prevent plagiarism or copying of solutions.
Before the **cross-check stage**, the repository **should be made public** so that other students can review and evaluate the code.

This approach ensures:

- equal conditions during development
- no access to other students’ solutions before submission
- full code visibility during cross-check and review

# Branching and Project Setup

- In the private repository, create a branch named `online-zoo`
- Inside this branch, create a folder also named `online-zoo`. Place all project files inside this folder
- The `main` (or `master`) branch should be **empty** (contain only files like README.md, .gitignore or .github folder)

# Project Structure

- At the root level of the project folder, create two main folders: `assets`, `pages`

```text
online-zoo/
├── assets/
└── pages/
```

**Assets Folder**  
The assets folder is used to store static resources such as: `images`, `icons`, `font files` (if applicable)  
An example structure for the assets folder:

```text
assets/
├── images/
├── icons/
└── fonts/
```

**Pages Folder**  
Inside the pages folder, create separate folders for each page.
Each page folder should contain the following files related to that specific page: `.html`, `.css`, `.js`
An example structure for the pages folder:

```text
pages/
├── landing/
│   ├── index.html
│   ├── style.css
│   └── script.js
...
```

# Deployment

The project **should be deployed** and accessible via a public link.  
You may use **any deployment platform** of your choice, for example:

- GitHub Pages
- Vercel
- Netlify
- or any other suitable hosting service

The choice of deployment tool does not affect the evaluation, as long as the deployed version of the project is available and works correctly.

# Commit History Requirements

- The commit history should clearly reflect the **development process** of the application.
- Commits should follow the commit message guidelines provided in the official [Course Documentation](https://rs.school/docs/en/git-convention#commit-requirements)

# Requirements for Pull Requests

- Create a Pull Request from the `online-zoo` branch to the `main` (or `master`) branch.
- Name the Pull Request according to the **task title**.
- Provide the Pull Request description following the [Required Template](https://rs.school/docs/en/pull-request-review-process#pull-request-requirements-pr)
- **DO NOT MERGE** the Pull Request into the `main` branch.

# How to Submit

After receiving the task and **before the deadline**, submit your work via the RS App:

- Go to the RS App: [https://app.rs.school/](https://app.rs.school/)
- Select **Cross-Check: Submit**.
- Choose the relevant task from the dropdown menu.
- Add the link to the deployed version of your website to the **Solution URL** field.
- Click the **Submit** button.

Detailed instructions for the cross-check process are available here: [Cross-check](https://rs.school/docs/en/cross-check-flow)

# Submit Recommendations

It is recommended to submit the task as early as possible, as soon as the option becomes available in the RS App.  
After submission, you may continue working on the task until the deadline.

Make sure that the deployed link you provide opens correctly in the browser’s incognito mode.

# General Technical Requirements

- The layout should be valid, semantic, and match the design.
- The application should be displayed correctly and function properly in the latest version of **Google Chrome**.
- The use of CSS frameworks (e.g., `Bootstrap`) is **not allowed**.
- The use of JavaScript frameworks (e.g., `Angular`, `React`, `Vue`, etc.) is **not allowed**.
- The use of outdated libraries (e.g., `jQuery`) or pre-built libraries (e.g., `Swiper`) to implement functionality is **not allowed**.
- The use of `TypeScript` is **not allowed**.
- The project should be implemented using **Vanilla JavaScript**.
- The use of CSS preprocessors (`SASS`, `SCSS`) and `normalize.css` is **allowed**.
- The use of a style reset such as `reset.css` is **not recommended**.
- Adding layout as an image (for example, taking a screenshot of part of the layout and inserting it into the markup) is **not allowed**.  
  Layout should be implemented using **HTML tags and characters**. Images may be used **only** for pictures and icons, not for layout elements (buttons, blocks, sections).
- The code should be **readable** without minification or obfuscation.

# Please Pay Attention to the Following Points

- The main layout blocks should be positioned **at the specified screen widths**, as shown in the Figma design.
- Images and logos (if any) should be placed within a **logical container**, using correct centering and positioning.  
  Minor deviations from the design are allowed if required by a grid or column-based layout.
- Icons and images should maintain **precise spacing** relative to the beginning of the corresponding text.
- There are separately designed blocks in the layout that demonstrate how a button should look **with a hover effect** and **without it**.
- If the correct font is used, check **the text height** - it should match the original design.
  The width may vary. However, it is common practice to apply the `letter-spacing` property to headings, mottos, or quotes.
- If there are several elements of visually equal width in a single row, the width of their containing blocks should also be equal.
- If there are headings or menu items written **ENTIRELY IN UPPERCASE**, make sure the `text-transform: uppercase;` property is applied.

❗ **Pixel-perfect accuracy is NOT required**.  
Small differences of a few pixels are acceptable **— matching proportions and visual consistency are what matter**.

“Interactive” means that an element displays a **visual effect or animation** (at your discretion: cursor animation, background color change, darkening, underline, font change) in response to user actions, for example, when hovering the cursor.
**Using JavaScript to handle user interactions in this task is not required.** Such effects are usually implemented using the `:hover` pseudo-class and the following properties:

- `cursor: pointer`,
- `background`,
- `text-decoration: underline`,
- `color`.

❗ **Examples of how buttons or blocks should behave on hover are provided in the design mockup.**

# Definition: "Layout Matches the Design"

"Layout matches the design" means that:

- all required elements are present,
- elements are arranged according to the design structure and visual intent,
- relative positioning and alignment of elements follow the design.
- **Minor visual deviations are acceptable**.

# Layout Requirements

### Evaluation criteria

Maximum score: **435**

## Layout validation — 20 points

- [ ] HTML markup is valid according to [https://validator.w3.org/](https://validator.w3.org/) — **(16 points total)**
  - No errors or warnings: **+2 points per page** (Home, Map, ZOOS, Contact Us)
  - Warnings only (no errors): **+2 points per page** (Home, Map, ZOOS, Contact Us)
- [ ] Favicon is added to all pages — **(+2)**
- [ ] Semantic HTML structure is used (header, main, section, footer) — **(+2)**

## Landing Page (104 points)

1. Responsive behavior — **(16 points total)**
   - [ ] Smooth resizing and progressive adaptation across required widths — **(+10)**
   - [ ] No overlaps / broken layout / cropped content — **(+4)**
   - [ ] No horizontal scrolling at required widths — **(+2)**

2. **Header** (`<header>` should contain only the logo, navigation menu, and social media icons) - **(10 points total)**
   - [ ] The logo should be positioned on the **left** - **(+2)**
   - [ ] The navigation menu should be **interactive**. By default, the first item `ABOUT` should be **highlighted** - **(+2)**
   - [ ] The social media icons panel should be **interactive** - **(+2)**
   - [ ] The page should contain an `<h1>` element (e.g. "Online Zoo") - **(+2)**
   - [ ] The header **should not be sticky**. When scrolling, it should remain in its original position - **(+2)**

3. Section **WATCH YOUR FAVORITE ANIMAL ONLINE** - **(7 points total)**
   - [ ] The `VIEW LIVE CAM` button should be **interactive** - **(+2)**
   - [ ] The background of this block should be an **image** - **(+5)**

4. Section **WELCOME TO THE ONLINE ZOO! / HOW WE WORK** - **(10 points total)**
   - [ ] Images should be positioned correctly relative to the text - **(+10)**

5. Section **YOUR DONATION MAKES A DIFFERENCE!** - **(7 points total)**
   - [ ] The `$ DONATION AMOUNT` button should have an **interactive** state - **(+2)**
   - [ ] All elements in this section should be present - **(+5)**

6. Section **MEET SOME OF OUR PETS** - **(18 points total)**
   - [ ] The left (`<`) and right (`>`) buttons should be **interactive** - **(+4)**
   - [ ] Animal cards should be **interactive** (at least the cursor should change). Clicking anywhere on a card should navigate to the animal page - **(+10)**
   - [ ] The `VIEW LIVE CAM` button inside each card should be **interactive** - **(+2)**
   - [ ] The `CHOOSE YOUR FAVORITE` button should be **interactive** - **(+2)**

7. Section **PAY AND FEED** - **(7 points total)**
   - [ ] The `DONATE NOW` button should be **interactive** - **(+2)**
   - [ ] All elements in this section should be present - **(+5)**

8. Section **WHAT OUR USERS THINK** - **(10 points total)**
   - [ ] The left (`<`) and right (`>`) navigation buttons should be **interactive** - **(+4)**
   - [ ] The `LEAVE FEEDBACK` button should be **interactive** - **(+2)**
   - [ ] All elements in this section should be present - **(+4)**

9. Section **CARE FOR THE ANIMALS YOU LOVE** - **(9 points total)**
   - [ ] Images without captions should **not** be interactive - **(+2)**
   - [ ] Animal cards should be **interactive** (at least the cursor should change).  
          Clicking anywhere on a card should navigate to the animal page - **(+5)**
   - [ ] The `CHOOSE YOUR FAVORITE` button should be **interactive** - **(+2)**

10. **Footer** (`<footer>` contains the navigation menu, logos, donation buttons, and social media icons) - **(10 points total)**

- [ ] The navigation menu should be **interactive**. By default, menu items should **not** be highlighted - **(+4)**
- [ ] The `DONATE FOR VOLUNTEERS` button should be **interactive** - **(+2)**
- [ ] The social media icons panel should be **interactive** - **(+4)**

## Map Page (56 points)

1. Responsive behavior — **(16 points total)**
   - [ ] Smooth resizing and progressive adaptation across required widths — **(+10)**
   - [ ] No overlaps / broken layout / cropped content — **(+4)**
   - [ ] No horizontal scrolling at required widths — **(+2)**

2. **Header** (`<header>` should contain only the logo, navigation menu, and social media icons) - **(10 points total)**
   - [ ] The logo should be positioned on the **left** - **(+2)**
   - [ ] The navigation menu should be **interactive**. By default, the first item `MAP` should be **highlighted** - **(+2)**
   - [ ] The social media icons panel should be **interactive** - **(+2)**
   - [ ] The page should contain an `<h1>` element (e.g. "Online Zoo") - **(+2)**
   - [ ] The header **should not be sticky**. When scrolling, it should remain in its original position - **(+2)**

3. Section **MAP** - **(20 points total)**
   - [ ] Animal icons should be positioned correctly relative to the map - **(+10)**
   - [ ] The map should be non-scalable (visual zoom via layout changes is allowed, but no interactive map scaling) - **(+10)**

4. **Footer** (`<footer>` contains the navigation menu, logos, donation buttons, and social media icons) - **(10 points total)**
   - [ ] The navigation menu should be **interactive**. By default, menu items should **not** be highlighted - **(+4)**
   - [ ] The `DONATE FOR VOLUNTEERS` button should be **interactive** - **(+2)**
   - [ ] The social media icons panel should be **interactive** - **(+4)**

## Zoos Page (133 points)

- Base Zoos Page (layout + logic) — **103 points**
- Each additional Zoos Page — **+10 points (maximum +30 points)**

### Requirements for a standard page

1. Responsive behavior — **(16 points total)**
   - [ ] Smooth resizing and progressive adaptation across required widths — **(+10)**
   - [ ] No overlaps / broken layout / cropped content — **(+4)**
   - [ ] No horizontal scrolling at required widths — **(+2)**

2. **Header** (`<header>` should contain only the logo, navigation menu, and social media icons) - **(10 points total)**
   - [ ] The logo should be positioned on the **left** - **(+2)**
   - [ ] The navigation menu should be **interactive**. By default, the first item `ZOOS` should be **highlighted** - **(+2)**
   - [ ] The social media icons panel should be **interactive** - **(+2)**
   - [ ] The page should contain an `<h1>` element (e.g. "Online Zoo") - **(+2)**
   - [ ] The header **should not be sticky**. When scrolling, it should remain in its original position - **(+2)**

3. Section **LIVE CAMS** - **(48 points total)**
   - [ ] A left-side animal navigation panel should be present - **(+2)**
   - [ ] The panel should support two states:
     - **expanded (opened)** state (animal icon, text description) - **(+2)**
     - **collapsed** state (only animal icons should be visible) - **(+2)**
   - [ ] The panel should be expandable and collapsible using the corresponding control - **(+4)**
   - [ ] The currently selected animal in the left panel should be **highlighted** in both states - **(+4)**
   - [ ] Clicking on an animal item should:
     - update the **visual highlight** in the side panel - **(+4)**
     - change the **active animal** displayed on the page - **(+4)**
   - [ ] When scrolling, the animal navigation menu should become **sticky** at the top of the screen. Refer to `position: sticky` for this behavior - **(+2)**
   - [ ] The `DONATE NOW` button should be **interactive** - **(+2)**
   - [ ] The main video preview should be either - **(+2)**:
     - **a YouTube preview**, or
     - redirect to a **YouTube page when clicked**.
   - [ ] The MORE LIVE VIEWS block should be displayed below the main video - **(+2)**
   - [ ] The MORE LIVE VIEWS carousel should contain preview images. Each preview should be either - **(+4)**:
     - **a YouTube preview**, or
     - redirect to a **YouTube page when clicked**.
   - [ ] The left (`<`) and right (`>`) navigation buttons should be **interactive** - **(+4)**
   - [ ] The currently selected camera preview should be **visually highlighted** - **(+2)**

4. Section **PAY AND FEED** - **(7 points total)**
   - [ ] The `$ DONATION AMOUNT` button should be **interactive** - **(+2)**
   - [ ] All elements in this section should be present - **(+5)**

5. Section **DID YOU KNOW?** - **(12 points total)**
   - [ ] Shadows around the block should be implemented using the `box-shadow` property, even if the visual result looks slightly different - **(+2)**
   - [ ] The `VIEW MAP` button should be **interactive** - **(+2)**
   - [ ] All elements in this section should be present - **(+8)**

6. **Footer** (`<footer>` contains the navigation menu, logos, donation buttons, and social media icons) - **(10 points total)**
   - [ ] The navigation menu should be **interactive**. By default, menu items should **not** be highlighted - **(+4)**
   - [ ] The `DONATE FOR VOLUNTEERS` button should be **interactive** - **(+2)**
   - [ ] The social media icons panel should be **interactive** - **(+4)**

7. When switching to other animal pages, the page corresponds to the Figma design, and interactive elements function correctly- **(+30)**

## Contact Us (62 points)

1. Responsive behavior — **(16 points total)**
   - [ ] Smooth resizing and progressive adaptation across required widths — **(+10)**
   - [ ] No overlaps / broken layout / cropped content — **(+4)**
   - [ ] No horizontal scrolling at required widths — **(+2)**

2. **Header** (`<header>` should contain only the logo, navigation menu, and social media icons - **(10 points total)**
   - [ ] The logo should be positioned on the **left** - **(+2)**
   - [ ] The navigation menu should be **interactive**. By default, the first item `CONTACT US` should be **highlighted** - **(+2)**
   - [ ] The social media icons panel should be **interactive** - **(+2)**
   - [ ] The page should contain an `<h1>` element (e.g. "Online Zoo") - **(+2)**
   - [ ] The header **should not be sticky**. When scrolling, it should remain in its original position - **(+2)**

3. Section **GET IN TOUCH** - **(26 points total)**
   - [ ] The contact form structure and layout should match the design and include the following fields: `Your Name`, `Your Email Address`, `Subject`, `Message` - **(+20)**
   - [ ] All required fields should be clearly marked (e.g. with an asterisk `*`) - **(+2)**
   - [ ] Each form field should include a **placeholder text**, as shown in the design - **(+2)**
   - [ ] The `SEND MESSAGE` button should be **interactive** - **(+2)**

4. **Footer** (`<footer>` contains the navigation menu, logos, donation buttons, and social media icons) - **(10 points total)**
   - [ ] The navigation menu should be **interactive**. By default, menu items should **not** be highlighted - **(+4)**
   - [ ] The `DONATE FOR VOLUNTEERS` button should be **interactive** - **(+2)**
   - [ ] The social media icons panel should be **interactive** - **(+4)**

## Donation Popup "TOGETHER WE CARE, SAVE AND PROTECT!" (20 points)

1. Popup behavior & overlay - **(10 points total)**
   - [ ] Popup opens above page content and is centered on the screen - **(+2)**
   - [ ] Page scrolling is disabled while the popup is open - **(+2)**
   - [ ] Background page is visually dimmed using an overlay - **(+2)**
   - [ ] Smooth resizing and progressive adaptation across required widths — **(+4)**

2. Popup structure & layout - **(6 points total)**
   - [ ] Popup layout matches the design (image, title, text, buttons) - **(+4)**
   - [ ] Close button (`×`) is positioned according to the design - **(+2)**

3. Interactivity - **(4 points total)**
   - [ ] Donation amount buttons are interactive (hover + cursor change) - **(+2)**
   - [ ] Close button (`×`) is interactive and closes the popup - **(+2)**

## Donation Popup "MAKE YOUR DONATION" Step 1–3 (40 points)

### Requirements for the first step (22 points)

- [ ] Popup opens above page content and is centered on the screen - **(+2)**
- [ ] Page scrolling is disabled while the popup is open - **(+2)**
- [ ] Background page is visually dimmed - **(+2)**
- [ ] Popup demonstrates smooth resizing and progressive adaptation across required screen widths - **(+2)**
- [ ] Popup layout matches the design - **(+4)**
- [ ] Buttons are interactive - **(+4)**
- [ ] `FOR SPECIAL PET` dropdown: opens/closes correctly, selected item is highlighted - **(+4)**
- [ ] Step indicator updates correctly when progressing - **(+2)**

### Requirements for the second step (9 points)

- [ ] Popup remains centered above page content - **(+1)**
- [ ] Page scrolling remains disabled - **(+1)**
- [ ] Overlay remains visible and unchanged - **(+1)**
- [ ] Smooth adaptive behavior across required widths - **(+1)**
- [ ] Popup layout matches the design - **(+2)**
- [ ] Required fields are visually marked (e.g. `*`) - **(+1)**
- [ ] Buttons are interactive - **(+2)**

### Requirements for the third step (9 points)

- [ ] Popup remains centered above page content - **(+1)**
- [ ] Page scrolling remains disabled - **(+1)**
- [ ] Overlay remains visible and unchanged - **(+1)**
- [ ] Smooth adaptive behavior across required widths - **(+1)**
- [ ] Popup layout matches the design - **(+2)**
- [ ] Required fields are visually marked (e.g. `*`) - **(+1)**
- [ ] Buttons are interactive - **(+2)**

# Specifics of Layout Verification

1. A deviation of up to **10px horizontally and vertically is allowed**, provided that the overall visual similarity between the layout and the implementation is preserved.
2. The [PerfectPixel](https://chromewebstore.google.com/detail/perfectpixel-by-welldonec/dkaagdgjmgdmbnecmcefdhjekcoceebi?hl=en) browser extension may be used as a **supporting tool** to verify layout conformity.
3. When checking the layout with PerfectPixel, ensure that:
   - the extension scale is set to 1:1,
   - the browser zoom is set to 100%,
   - the operating system scaling is set to 100%.
4. If the screen resolution is **greater than 1440px**, it is sufficient to horizontally center the layout or manually align it with the top-left corner guides for verification.
5. If the screen resolution is **1440px or less**, use the **Device Toolbar in Google Chrome** in responsive mode to perform the check.  
   Refer to the **DevTools Responsiveness Check section** below for detailed usage instructions.
6. Please note that when checking the layout at a window width of **1440px**, the layout may shrink by approximately **17px**. This occurs because part of the available space is occupied by the browser’s vertical scrollbar (17px is the standard scrollbar width in Google Chrome).
7. Each block and section is reviewed **independently**. Issues found in a previous block do not affect the evaluation of subsequent blocks. When moving to the next block, align it again with the overlaid layout.
8. For text content, we verify:
   - alignment and spacing relative to the block boundaries,
   - text height only.

Differences in word width or letter spacing between the design and the implementation are **not considered errors**, provided that the correct font and specified font properties are used.

# Penalties

- **Layout implemented using images instead of HTML/CSS**  
  (for example, screenshots of layout blocks inserted as images instead of proper markup): **–90 points**

- **Using frameworks, libraries, or technologies prohibited by the technical requirements**
  (CSS frameworks, JavaScript frameworks, TypeScript, outdated or pre-built libraries): **–90 points**

# DevTools Responsiveness Check

1. Open Developer Tools
   - Open Developer Tools using one of the following methods:
     - macOS: `Cmd + Option + I`
     - Windows / Linux: `Ctrl + Shift + I`
     - or right-click anywhere on the page and select **Inspect**
   - Click the **Toggle Device Toolbar** icon in the top-left corner of the DevTools panel.
   - In the device toolbar, select **Responsive** mode

2. Make sure there is no horizontal scrollbar in **Responsive** mode. If a scrollbar is present:
   - Switch the device type from `Desktop` to `Mobile` in the Device Toolbar panel
   - If the device type is not displayed, click on the three dots (`⋮`) on the right side of the Device Toolbar panel and select `Add device type`

3. Set the screen width to the required values specified in the task description and check the layout against the Figma design. If the page does not reflow correctly or white space appears on the right, you may need to refresh the page

4. Check the layout for compliance with the Figma design.

5. To check responsiveness at different screen widths, smoothly change the viewport width in DevTools from the maximum (1920px) to the minimum (320px). Make sure there is no horizontal scrollbar at any width. If a scrollbar or white space appears on the right, try refreshing the page, as the layout may not have updated correctly

6. When browser zoom is applied (for example, 125%), the actual viewport width may differ by 1–2 pixels. For instance, a width set to 768px may appear as 767px or 769px. In such cases, evaluate the layout at the nearest breakpoint transition point rather than relying on the exact numeric value.

7. Check that hover effects on interactive elements are disabled in the `Mobile` device type. To do this, tap or click an interactive element and ensure it does not remain in a hover state. Then switch to the `Desktop` device type to verify that hover effects are enabled and work correctly.

**The image below shows an example of a horizontal scrollbar visible in Responsive mode:**

![DevTools scrollbar example](https://user-images.githubusercontent.com/73646765/223966120-845e2526-c54c-4611-8173-db5f9a2c3faa.png)

# Useful links

lemented using images instead of HTML/CSS**  
 (for example, screenshots of layout blocks inserted as images instead of proper markup):**–90 points\*\*

- **Using frameworks, libraries, or technologies prohibited by the technical requirements**
  (CSS frameworks, JavaScript frameworks, TypeScript, outdated or pre-built libraries): **–90 points**
