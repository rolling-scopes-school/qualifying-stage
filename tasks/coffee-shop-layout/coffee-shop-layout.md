# Coffee House

## Project's Description
Coffee House is a project where you will need to create a website consisting of two pages, make it responsive, and add interactivity.
The duration of the task is 2 week.  
The form of evaluation of the task is a cross-check review.
[Design in Figma](https://www.figma.com/file/SAoBmuOqTfguehdT4IFRxQ/Coffee-House?type=design&node-id=0-1&mode=design&t=qis81E9Ovgx47eVl-0)


## Key skills
- Valid semantic responsive web design;
- Easy-to-maintain readable code;
- Exporting styles and graphics from Figma;
- Using JavaScript to implement the functionality specified in the task.


## Creating your own copy of the layout
Start the task by creating your own copy of the layout. To do this:
- Log in to [Figma](https://www.figma.com/);
- Open the layout;
- On the top panel, click on the arrow next to the layout name, and select the option "Duplicate to your drafts";
- At the top left, open the settings, and choose "Back to files";
- Open the copy of the layout with the label "In Drafts".


## Technical requirements
1. The layout is valid, semantic, and matches the design.
2. The application is displayed correctly and functions properly in the latest version of Google Chrome.
3. Using CSS frameworks (e.g., `Bootstrap`) **is not allowed**.
4. Using JS frameworks (e.g., `Angular`, `React`, `Vue`, etc.) **is not allowed**.
5. Using outdated libraries (e.g. `JQuery`, etc.) or pre-built libraries (e.g. `Swiper`, etc) to implement functionality **is not allowed**.
6. Using `TypeScript` **is not allowed**.
7. Using CSS preprocessors (`SASS`, `SCSS`), `normalize.css` is allowed.
8. Using a style reset with `reset.css` is not recommended.
9. Adding layout as an image by taking a screenshot of a part of the layout and pasting it into the markup is not allowed. Please use tags and characters for layout, and use images only for adding pictures and icons, not for layout elements (buttons, blocks, sections).
10. The code must be readable, without minification or obfuscation.

## Repository Requirements
- Task should be done in private school's repository
- Create new branch `coffee-house` from `main`. Create a folder `coffee-house` in the created branch. Place your code in this folder.
- The `main` (or `master`) branch should be empty (contain only files like README.md, .gitignore or .github folder)
- Use `gh-pages` for deployment
- Upon completing the assignment, create a Pull Request from the `coffee-house` branch to the `main` branch

  **NOTE: DO NOT perform the Merge**

- The internal structure of the project is at your discretion. The simplest option is separate pages, each with its own styles and js. When submitting the work, please ensure that the provided submission link opens the main page of the deployed project

## Commit Requirements
- Commit history should reflect the application development process.
- [Give commit names according to the guideline](https://docs.rs.school/#/en/git-convention)

## Requirements for Pull Requests
- Name the Pull Request according to the task title
- [Provide the Pull Request description following the template](https://docs.rs.school/#/en/pull-request-review-process?id=pull-request-requirements-pr)  
  **No need to merge the Pull Request from the development branch into the `main` branch**.

## How to submit
After receiving the task but before the deadline, please go to the RS App at https://app.rs.school/. Select **Cross-Check: Submit**, choose the relevant task from the dropdown menu, and add the link to the deployed version of your created website in the **Solution URL** field. Then, click **Submit** button.

## Submit Recommendations
- It is recommended to submit the task as early as possible, as soon as the option becomes available in the rs app. After submission, you can continue working on the task until the deadline
- Since the project is being done in a private repository, there is no point in submitting a link to the repository or a pull request - the reviewer won't be able to see it. The private school repository is only visible to you, course admins, and your mentors when they become available
- Make sure that the deployed link you provide opens in incognito mode of the browser

## Layout Requirements
1. Checking validation of pages: **+16**
    - The layout of both pages is valid: to check the validity of the layout, use the service https://validator.w3.org/ . **+12** (6 points per page)  
      Valid markup of checked page corresponds to the message "Document checking completed. No errors or warnings to show." In this case, we assign the full points for the checked page (+6). If there are `warnings` but no `errors`, we assign half of the points (+3) for the checked page
    -  Favicon is added to each page **+4**
2. The layout of the pages matches the design at a screen width of 1440px: **+14**
    - `<header>` block on each page **+2**
    - `Enjoy` block on `home` page **+2**
    - `Favourites Coffee` block on `home` page **+2**
    - `About` block on `home` page **+2**
    - `Mobile App` block on `home` page **+2**
    - `Menu` block on `menu` page **+2**
    - `<footer>` block on each page **+2**
3. The layout of the pages matches the design at a screen width of 768px: **+14**
    - `<header>` block on each page **+2**
    - `Enjoy` block on `home` page **+2**
    - `Favourites Coffee` block on `home` page **+2**
    - `About` block on `home` page **+2**
    - `Mobile App` block on `home` page **+2**
    - `Menu` block on `menu` page **+2**
    - `<footer>` block on each page **+2**
4. The layout of the pages matches the design at a screen width of 380px: **+14**
    - `<header>` block on each page **+2**
    - `Enjoy` block on `home` page **+2**
    - `Favourites Coffee` block on `home` page **+2**
    - `About` block on `home` page **+2**
    - `Mobile App` block on `home` page **+2**
    - `Menu` block on `menu` page **+2**
    - `<footer>` block on each page **+2**
5. There is no horizontal scroll bar at all screen width up to 380px inclusive. All page content remains as per the design: it is not cropped, removed, or shifted to the side: **+20**
    - No horizontal scroll bar when the `home` page width is between 1440px and 768px: **+5**
    - No horizontal scroll bar when the `home` page width is between 768рх and 380рх: **+5**
    - No horizontal scroll bar when the `menu` page width is between 1440px and 768px: **+5**
    - No horizontal scroll bar when the `menu` page width is between 768рх and 380рх: **+5**
6. During smooth resizing of the screen from 1440px to 380px, the layout takes up the full width of the window (including the margins specified in the layout), elements change their sizes and positions (but without full scaling), elements do not overlap, and images maintain their correct proportions: **+8**
    - On `home` page: **+4**
    - On `menu` page: **+4**
7. At screen widths of 768px and below on both pages, the menu and navigation buttons in the header are hidden, and a burger menu icon appears: **+4**  
   Opening the menu by clicking on the burger menu icon is not checked at this stage
8. Hover effects are enable on desktop devices (`Desktop` device type in DevTools) and disabled for mobile devices on both pages (`Mobile` device type in DevTools): **+4**
9. CSS Requirements **+10**
    - For positioning images in `About` block on `home` page and products in `Menu` block on `menu` page used **Flexbox** or **Grid Layout** **+4**
    - When scaling the browser page (<100%) or increasing the page width (>1440px), the layout of both pages is centered rather than shifted to the side and not stretched across the entire width **+4**
    - The background color **Body** stretches across the entire width of the page **+2**
10. Interactivity **+32**
    - Navigation elements (except `Contacts`) lead to corresponding blocks on `home` page (anchor links) **+4**
    - `Contacts` in navigation panel links to the `<footer>` block on its own page (anchor link) **+2**
    - Smooth scrolling with anchor links **+2**
    - When clicking on the **Menu** buttons in `header` and `Enjoy` block on `home` page, it navigates to the `menu` page **+2**
    - The **Menu** button in `header` on `menu` page is non-interactive **+2**
    - When clicking on the **Logo** in `header`, it navigates to the `home` page **+2**
    - The active **Coffee** button in `Menu` block of `Menu` page is non-interactive **+2**
    - Each Coffee-card in the `Menu` section of the `Menu` page is interactive when hovering over any area of the card **+4**
    - In the `<footer>` block, clicking on the link with phone number (all area including icon) should initiate a phone call **+2**
    - In the `<footer>` block, clicking on the link with the address (all area including icon) should open a new browser tab with Google Maps displaying any location of your choice **+2**
    - Interactivity of links and buttons is implemented according to Figma layout. Interactivity includes not only changing cursor's appearance, for example, using the `cursor: pointer` property, but also the use of other visual effects, such as changing the background color or font color, following the **Styleguide** in Figma layout **+4**
    - Mandatory requirement for interactivity: smooth change in the appearance of an element on hover and click, without affecting adjacent elements **+4**
11. At screen widths of 768px and below on both pages, the menu and navigation buttons in the header are hidden, and a burger menu icon appears: **+4**  
12. Hover effects are enable on desktop devices (`Desktop` device type in DevTools) and disabled for mobile devices on both pages (`Mobile` device type in DevTools): **+4**

##Functional requirements

1. Implementation of the burger menu on both pages: **+22**
    - At a page width of 768px or less, the navigation panel hides, and the burger icon appears: **+2**
    - When clicking the burger icon, the burger menu slides out from the right, and the burger icon smoothly transforms into a cross: **+4**
    - The burger menu occupies the entire available screen area below the `<header>` block: **+2**
    - When clicking the cross, the burger menu smoothly hides, moving to the right of the screen, and the cross smoothly transforms into a burger icon: **+4**
    - The burger icon is created using HTML and CSS without the use of images: **+2**
    - Links in the burger menu work, providing smooth scrolling to anchor points: **+2**
    - When clicking on any link (interactive or non-interactive) in the menu, the burger menu smoothly hides to the right, and the cross smoothly transforms into a burger icon: **+2**
    - The placement and dimensions of elements in the burger menu match the layout (horizontal centering of menu items): **+2**
    - When the page width increases to 769px or higher, the burger icon and the open burger menu hide, and the navigation panel appears: **+2**
2. Implementation of the carousel on the `home` page: **+24**
    - Carousel elements are automatically scroll to the left with a specified time interval by default. The time interval duration is at the student's choose, but the recommended value is 5-7 seconds: **+4**
    - The current state until the next automatic switch is shown in the progress bar of the corresponding slide by filling it with color: **+4**
    - Only the progress bar of the current slide can be filled; the rest remain in their default state: **+2**
    - When hovering the mouse or touch-and-hold on the displayed carousel element, the time to the element switch is paused. When the mouse cursor moves out, or the hold ends, the time continues from where it stopped: **+2**
    - The switch slides is accompanied by like the carousel animation (the method of animation execution is not verified): **+4**
    - Manual switching in the corresponding direction is implemented by pressing left arrow button or right arrow button: **+2**
    - For mobile devices, manual switching in the corresponding direction is additionally implemented by swiping left or right: **+2**
    - When manually switching, the progress bar state of the switched slide resets, and the progress bar of the displayed slide starts to fill: **+2**
    - When switching to the right after the third element, it returns to the first. When switching to the left after the first element, it returns to the third: **+2**
3. Categories of products on the `menu` page: **+16**
    - The **Coffee** category is active and the corresponding products are displayed when opening or reloading the `menu` page: **+2**
    - When switching categories, the products of the selected category are displayed: **+2**
    - For screens with a width of 768px or less, when opening/reloading the page or switching categories, only 4 products are displayed. If there are more than 4 products in the displayed category, a **Load More** button is displayed below: **+4**
    - When clicking the **Load More** button below the displayed products, the missing products are added, and the **Load More** button is hidden: **+4**
    - When changing the screen width, the product display mode (8 products per page or 4 products with a **Load More** button) changes without page reloading: **+4**
4. The Modal on the `menu` page: **+20**
    - The Modal with the description of a specific product opens when clicking on any part of a card of product: **+2**
    - The part of the page outside the Modal is darkened: **+2**
    - When the Modal is open, the vertical scroll of the page becomes inactive; when closed, it becomes active again: **+2**
    - Clicking on the area around the Modal and **Close** button closes it: **+2**
    - The Modal is centered on both axes, sizes of modal elements and their layout match the design: **+2**
    - After the Modal is opened, the 'Size' option 'S' is selected, and no option in the 'Additives' section is selected. The product's final price is the same as in the card: **+2**
    - Only one 'Size' option can be selected. Changing this option also changes the final price of the product based on the choice (+$0.00 for **S**, +$0.50 for **M**, +$1.00 for **L**): **+4**
    - Multiple 'Additives' options can be selected, and each selected option increases the final price of the product by $0.50: **+4**
5. Video on the `home` page: **+8**
    - In the `Enjoy` block of the `home` page, a video is played in the background instead of an image, without sound and control elements, and without the ability to interact with it: **+4**
    - After the video is finished, it automatically starts over: **+4**

## Criteria for evaluation

**Maximum score for the task: 234 points**

Scores for requirement points are specified in [Layout Requirements](#layout-requirements) and [Functional requirements ](#functional-requirements) sections

All disputed issues are resolved in favor of the student being assessed.

To make the assessment of your work easier, print self-assessment of your project in the browser console, listing points for each criteria you have completed.

## Penalties
1. Layout of the entire design or individual blocks is implemented using images -90
2. Using frameworks, libraries, and technologies prohibited in technical requirements -90

## Task Evaluation
- The assignment is assessed through a cross-check
- Instructions for conducting a cross-check: https://docs.rs.school/#/en/cross-check-flow

## Specifics of verifying layout
- Deviation from the layout of up to 10px horizontally and vertically is allowed, provided that the visual similarity between the layout and the markup is maintained.
- Use the [PerfectPixel](https://chrome.google.com/webstore/detail/perfectpixel-by-welldonec/dkaagdgjmgdmbnecmcefdhjekcoceebi?hl=ru) extension as a tool to check the layout's conformity with the design
- When checking the layout using the PerfectPixel extension, make sure that the extension is set to a scale of 1, while the browser and operating system are set to a scale of 100%.
- If the screen resolution is greater than 1440 pixels, to check for compliance with the layout, it is sufficient to center horizontally the layout or manually align it with the top-left corner guides.
- If the screen resolution is 1440 pixels or less, use the device toolbar in Google Chrome browser in responsive mode for checking.
- Please note that when checking the work in a window with a width of 1440 pixels, the layout may compress by approximately 17 pixels. This happens because part of the layout space is consumed by the vertical scroll (17 pixels - the standard scroll size for Google Chrome).
- Each block and section are reviewed separately, meaning that shortcomings in the previous block do not carry over to next one. When transitioning to the review of the next block, we align it with overlaid layout.
- Regarding text, we check its alignment and spacing relative to the block's boundaries. Text sizes are only checked for height. Deviations in word width and letter spacing when comparing the layout and the markup are not considered errors if the correct font with the specified properties is used
- The disappearance of the two images in the `About` block of the `home` page can occur at any point between 1440px and 768px

## DevTools responsiveness check details
1. Open Developer Tools:
    - Press the `F12` key on Mac or `Ctrl+Shift+i` on Windows or right-click and choose the `View Source` option in the context menu;
    - Click on the **Toggle device toolbar** icon in the top right corner of the developer tools panel;
    - Choose **Responsive** on the top panel.
2. Make sure there is no vertical scrollbar in **Responsive** mode. If a scrollbar is present, remove it by following these steps:
    - Switch the device type from `Desktop` to `Mobile` in the Device Toolbar panel;
    - If the device type is not displayed, click on the three dots on the right in the Device Toolbar panel and select `Add device type`
2. Set the screen width to the required value according to the task description, at which we will check the layout against the Design from Figma. If the page of the website being checked does not reformat, or if there is a white space on the right, you may need to refresh the page several times.
3. Check the layout for compliance with the Design.
4. For check responsiveness at different screen widths, smoothly change the screen width in DevTools from maximum (1440px) to minimum (380px), and make sure there is no horizontal scroll bar at any screen widths. If a scroll bar appears or white space appears on the right, try refreshing the page; perhaps the layout didn't update.
5. When scaling the screen (e.g., zoom + 125%), the actual width may differ by 1-2 pixels. For example, the actual value may be 767 or 769, even though the developer tools show 768. Therefore, you should adjust to the transition point, despite the difference.
6. Check that hover effects on interactive elements are disabled in the `Mobile` device type. To do this, click on an interactive element and ensure it does not remain in a hover state. Switch to the `Desktop` device type to verify that hover effects are enabled.

![image](https://user-images.githubusercontent.com/73646765/223966120-845e2526-c54c-4611-8173-db5f9a2c3faa.png)