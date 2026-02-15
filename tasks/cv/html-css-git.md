# CV. HTML, CSS & Git Basics

Your task is to create a branch named `rsschool-cv-html` from the `gh-pages` branch of the `rsschool-cv` repository,
add files `index.html` and `style.css`, which should include templates and corresponding styles.

## CV Contents:

### EPAM HR Department Recommendations

1. Full Name
2. Contact Information
3. Brief Self-Introduction (your goals and priorities, emphasize your strengths, describe your work experience if applicable, or your desire to learn and acquire new skills)
4. Skills (programming languages, frameworks, methodologies, version control systems, and development tools you are proficient in)
5. Code Examples
6. Work Experience (Junior Devs can list educational projects with the skills used and links to the source code)
7. Education (including completed courses and training)
8. English Language (your English proficiency level, and if you had language practice, describe it)

## CV Writing Recommendations:

- CV design is up to you. Strive to make it of high quality. You can refer to the examples provided in the task materials for CV design inspiration.
- The CV should be in English.
- It is recommended to include real data in the CV.
- Add your photo or avatar to the CV. A photo is preferable.
- Specify up-to-date contact information, including your Discord server nickname.
- As a code example, provide a solution to a problem from [Codewars](https://www.codewars.com/).
- Add code using symbols and tags, not images.
- For completed projects, include the project's name, a link to the project's code on GitHub, or a link to the project's page. If you haven't completed any projects yet, use this CV as your first project.

## Technical Requirements:

- The work will be evaluated in the latest version of Google Chrome.
- There are no restrictions on using JavaScript libraries, preprocessors, frameworks, or any well-known technologies.

## Some of the validation rules:

- Extra spaces at the end of lines are not allowed.
- A closing tag or closing slash for a non-pair tag is not allowed.
- If you use characters `<`, `>`, `&`, etc., they must be replaced with escape sequences.

All errors found by the validator during the checking of your work are listed in the `Details` section of the results table.

## Workflow

1. In your GitHub account, create a public repository with the name `rsschool-cv`. In the main branch of this
   repository (`main`), there should be only one file, `README.md`.
2. Create a branch `gh-pages` from the `main` branch.
3. Create a branch `rsschool-cv-html` from the `gh-pages` branch.
4. Maintain a commit history during the project. Follow the [commit guideline](https://docs.rs.school/#/en/git-convention), where the name of each commit should start with one of the specified prefixes: `init:`, `feat:`, `fix:`, `refactor:`, `docs:`.
5. In the `rsschool-cv-html` branch, place the files `index.html` and `style.css`, adding templates with content to them.
6. In the `README.md` file of the `rsschool-cv-html` branch, add a link like `https://GITHUB-USERNAME.github.io/rsschool-cv/`, replacing `GITHUB-USERNAME` with your GitHub username. This link will open the CV page as a fully styled webpage
7. Create a Pull Request from the `rsschool-cv-html` branch to the `gh-pages` branch. The title of the Pull Request should be `HTML, CSS & Git Basics`. Follow the [Pull Request description template](https://docs.rs.school/#/en/pull-request-review-process?id=Требования-к-pull-request-pr). Merge the Pull Request from the `rsschool-cv-html` branch to the `gh-pages` branch.

## How to Submit the CV. Cross-Check Assignment

- The "CV. HTML, CSS & Git Basics" assignment is evaluated through cross-check.
- After receiving the task, but before the cross-check deadline, go to rs app https://app.rs.school/,
  select **Cross-Check: Submit**, choose the task name from the drop-down list, add the link to the deployed version
  of your CV in the **Solution URL** field, and click the **Submit** button.
- It is recommended to submit the assignment as soon as possible, as soon as it becomes available in rs app.
- You can continue working on the assignment after submission until the deadline.

## Evaluation Criteria: CV Deployment Task

**Maximum Score:** **+130**

### Submission

- **+10 points**: The student **submits a link** to their CV deployed on `gh-pages` through the [RS App](https://app.rs.school/course/student/cross-check-submit).

### Markup Validity

- **+10 points**: The HTML markup is valid.
  - Use the [W3C Markup Validator](https://validator.w3.org/) to check validity.
  - Full score (+10 points) is awarded if the validator displays:  
    _"Document checking completed. No errors or warnings to show."_
  - If the markup has **warnings** but no **errors**, students will earn **half** the points (+5).

### Semantic Markup

- **+20 points**: Semantic elements are used meaningfully in the HTML code:
  - **+5 points**: Includes `header`, `main`, and `footer` elements.
  - **+5 points**: Contains a `nav` element used appropriately.
  - **+5 points**: Includes only **one** `h1` heading in the document.
  - **+5 points**: Uses multiple `h2` headings to structure the content.

### Footer Content

- **+10 points**: The footer section must include:
  - A link to the **author's GitHub profile**.
  - The **year of creation**.
  - The course logo ([RS School logo](../cv/images/rs-school-logo.svg)).
  - A link to the [RS School course](https://rs.school/courses/short-track).

### CSS Styles

- **+10 points**: CSS is used to format the CV layout and design effectively.

### Responsive Design

- **+10 points**: The CV page remains horizontally centered when the browser window is resized, observing responsiveness best practices.

### Photo/Avatar

- **+10 points**: The CV must include an **author photo or avatar**:
  - The image **retains proper proportions** (no distortion).
  - Includes an **`alt` attribute** for accessibility.

### Lists Formatting

- **+10 points**: Navigation, contact information, and skills must use a **list structure**:
  - Allowed formats:
    - **Unordered list** (`ul > li` or `ul > li > a`).
    - **Ordered list** (`ol > li` or `ol > li > a`).

### CV Content

- **+30 points**: The CV includes the following sections:
  - **+5 points**: A brief **self-introduction**.
  - **+5 points**: **Contact information** (e.g., email, GitHub, LinkedIn).
  - **+5 points**: A list of **skills** relevant to the student.
  - **+5 points**: A **code example** added using proper HTML characters or code tags—not as an image.
  - **+5 points**: A **list of educational projects** with links to either the source code or deployed applications.
  - **+5 points**: Information about **education** and **English proficiency level**.

### Language Requirement

- **+10 points**: The CV content is written entirely in **English**, showcasing international standards.
