# Online Zoo: Business Functionality

In this task, you are required to add business logic to the previously created layout. Here’s what you’ll be implementing:
- Interaction with the back-end
- Fetching data for the user profile, donatation and animals
- Add a loader while waiting for the back-end response
- Error handling
- Creating **Registration** and **Sign-In** pages
- Add different views for registered and non-registered users
- Adding the functionality to **store card data**
- Communication with Local Storage

Link to the [layout](https://www.figma.com/file/lnK11foY8Aoa6oOlDXovVN/Online-ZOO-Project?node-id=0%3A1)

## Technical Requirements

1. The use of any frameworks or libraries is strictly **prohibited**.
2. **TypeScript Integration**
    - Add the **npm package TypeScript** to your application.
    - Create a `tsconfig.json` file for configuration.

3. **ESLint and Webpack/Vite Configuration**
    - ESLint should be configured to work with TypeScript.
    - Use the plugin `@typescript-eslint/recommended`.

4. **Browser Compatibility**
    - Ensure the application works in **Google Chrome**.

5. **Strict Typing**
    - All variables, function parameters, and methods should have defined types, including return types.
    - Interfaces should be actively used in the code.
    - Utilize TypeScript features such as enums, generics, and utility types.

6. **Configuration File Flags**
    - Ensure the following flags are present:
        - `"noImplicitAny": true`
        - `"strict": true`

7. **ESLint Rule**
    - Enable the ESLint rule: `no-explicit-any`.

8. **Back-end Compatibility**
    - Create all necessary interfaces to interact with the API.

## Repository Requirements

The assignment should be completed in your **own private repository**.  
During development, the repository **should remain private** to prevent plagiarism or copying of solutions.
Before the **cross-check stage**, the repository **should be made public** so that other students can review and evaluate the code.

This approach ensures:

- equal conditions during development
- no access to other students’ solutions before submission
- full code visibility during cross-check and review

## Commit Requirements
- Commit history should reflect the application development process.
- [Give commit names according to the guideline](https://docs.rs.school/#/en/git-convention)

## Requirements for Pull Requests
- Name the Pull Request according to the task title
- [Provide the Pull Request description following the template](https://docs.rs.school/#/en/pull-request-review-process?id=pull-request-requirements-pr)  
  **No need to merge the Pull Request from the development branch into the `main` branch**.

## How to submit
After receiving the task but before the deadline, please go to the RS App at https://app.rs.school/. Select **Cross-Check: Submit**, choose the relevant task from the dropdown menu, and add the link to the deployed version of your created website in the **Solution URL** field. Then, click **Submit** button.


## Functional Requirements

### Back-end integration
- Carefully review the endpoints provided by the backend and the corresponding interfaces. Use the [Swagger](https://vsqsnqnxkh.execute-api.eu-central-1.amazonaws.com/prod/docs#/)
  documentation for this

### Landing Page
1. **Data Fetching**
    - On page load, make requests to    the back-end to fetch data for the 
   ["Meet some our Pets"](https://vsqsnqnxkh.execute-api.eu-central-1.amazonaws.com/prod/pets) section and for the 
   ["What our users think"](https://vsqsnqnxkh.execute-api.eu-central-1.amazonaws.com/prod/docs#/default/get_feedback)

2. **Loader**
    - Show a loader while waiting for the back-end response at the location where the slider "Meet some our Pets" and 
   "What our users think" will appear. All other page elements should be immediately available.

3. **Error Handling**
    - If an error occurs, display the text: _“Something went wrong. Please, refresh the page”_ instead of the loader.

4. **Slider**
    - Implement a slider that allows users to navigate through the Pets and Feedback items using left and right arrows.
    - The slider should loop infinitely, meaning that navigating past the last item should bring the user back to the 
   first item, and vice versa.
    - All slider items should be programmatically generated using TypeScript and added to the page


### Header
1. **User icon**
    - Add user icon to the header at the right after the social icons. For logged in users, display their name next to 
   the icon.
   - If user has not been logged in, clicking the user icon should open popup with 2 options: Sing In and Registration 
   each of them should redirect to the Sign In or Registration page.
   - For logged in users, clicking the user icon should open a popup (menu) with options:
        - Profile information ( Name, Email )
        - Sign Out button
   - Design of icon and popup is up to you.

### Zoos Page
1. **Data Fetching**
    - On page load, make a [request](https://vsqsnqnxkh.execute-api.eu-central-1.amazonaws.com/prod/cameras) 
   to the back-end to fetch camera's data for Pets. This includes:
        - Description,
        - Id
    - Images. Create a folder containing all images and link them to each product using its unique ID. For images not
      included in the design, add them manually by selecting visuals that correspond to the product name.

2. **Loader**
    - While waiting for the back-end response, display a loader.
        - The header, main title, and footer must remain immediately accessible and stick to the top and bottom of the page, respectively.

3. **Error Handling**
    - Display the text: _“Something went wrong. Please, refresh the page”_ in place of the loader in case of an error.
    - The design of the notification is entirely up to you

4. **Side menu**
    - Side menu should be programmatically generated using TypeScript and added to the page.

5. **Did you know?**:
    - By default, only the first pet is selected, and Did you know? section filled accordingly.
    - When another pet is selected, the Did you know? section updated accordingly.


### Did you know? section
1. **Data Fetching**
    - When a user clicks on a pet in the side menu, make a back-end [request](https://vsqsnqnxkh.execute-api.eu-central-1.amazonaws.com/prod/docs#/default/get_pets__id_)  
   to fetch detailed information by its `id` and display it in the section.

2. **Section**
   - Section should be programmatically generated using TypeScript and added to the page.
   
3. **Loader**
    - While waiting for the back-end response, show an overlay with a loader.

4. **Error Handling**
   - Display the text: _“Something went wrong. Please, refresh the page”_ in place of the loader in case of an error.

5. **Opening the modal window**
   - When the user clicks the "View Map" button, open a modal window displaying a map centered on the pet's area. Modal 
window should contain a cross button at the right top corner to close the modal. Pay attention you firstly need to 
   research and choose a map service to implement this functionality (e.g., Google Maps, Leaflet and so on)

6. **Closing the Modal**
    - The modal closes upon:
        - Clicking the **close icon**, or
        - Pressing the **Esc key**.
        - Clicking outside the modal does close it.


### Make your donation popup
1. **Step 1**
   - The Next button should remain disabled until the user selects a donation amount—either by choosing one of the 
   suggested options or by entering a value in the Other amount input field.
   - Once the user selects or enters a donation amount and chooses a pet from the For special pet dropdown, enable the 
   Next button to allow progression to Step 2.
   - Add validation to the Other amount input to accept only numeric values greater than 0. Scientific notation 
   (e.g., 1e5, 2e-4) should not be permitted.
   
2. **Step 2**
    - If user has been logged in before opening the popup, prefill the **Step 2** form with the user's name and email
    - Add validation to the input fields:
        - Name: Should contain only letters (both uppercase and lowercase) and spaces. No numbers, special characters, 
      or punctuation are allowed.
        - Email: Should follow the standard email format
    - The **Donate** button should remain disabled until both fields are correctly filled.

3. **Step 3**
   - Please **DO NOT USE THE REAL PAYMENT INFO FOR TESTING PURPOSES**
    - Add validation for card info
      - Card Number: Should be exactly 16 digits long and contain only numeric characters.
      - Expiration Date: Should be in the format MM/YY and represent a valid future date.
      - CVV: Should be exactly 3 digits long and contain only numeric characters.
    - The **Donate** button should remain disabled until all fields are correctly filled.
    - If user has been logged in before opening the popup, add checkbox "Save card info for future donations"
    - If user has at least one saved card, display saved cards above the card info form for selection ( dropdown with 
   card names created from the card number e.g. 1234 **** **** 5678 ). If user selects one of the saved cards, prefill 
   the card info form with the saved data.
    - This info should be stored in Local Storage only if user checked the "Save card info for future donations" checkbox.

4. **Complete donation**
   - As soon as the user clicks the **Complete donation** button on Step 3, sent data to the [back-end](https://vsqsnqnxkh.execute-api.eu-central-1.amazonaws.com/prod/docs#/default/post_donations)
   and display a thank-you message within the notification in success case:
   _"Thank you for your donation of [amount] to [pet name]!"_ or an error message in case of failure:
   _"Something went wrong. Please, try again later."_
   - Design of the message and notification is up to you.


### Sign In Page
1. **Input Fields**
    - The user should input their **login** and **password**.

2. **Validation Rules**
    - **Login Rules**:
        - Should be at least 3 characters long.
        - Should start with a letter.
        - Only English alphabet letters are allowed.

    - **Password Rules**:
        - Should be at least 6 characters long.
        - Should contain at least 1 special character.

3. **Validation effects**
    - On blur, validate the input field. If invalid:
        - Apply a red border and error icon to the input.
        - Display a validation message below the field.
    - On focus, clear the validation message and reset the input styling.

4. **Button Enablement**
    - The **Sign In** button should remain disabled until both fields are correctly filled.

5. **Authentication**
    - On clicking the **Sign In** button, send a [request](https://vsqsnqnxkh.execute-api.eu-central-1.amazonaws.com/prod/docs#/default/post_auth_login) 
   to the back-end to authenticate the user.

6. **Error Handling**
    - If the login attempt fails, display an error message below the form: _“Incorrect login or password”_.

7. **Successful Login**
    - Upon successful login, redirect the user to the **Menu** page.

### Registration Page
1. **Input Fields and Validation**
    - **Login**:
        - At least 3 characters, start with a letter, only English letters are allowed.

    - **Password & Confirm Password**:
        - At least 6 characters and should contain at least 1 special character.
        - The two fields should match (case-sensitive).

    - **Name**:
        - At least 3 characters, only English letters are allowed

2. **Mandatory Fields**
    - All fields should be filled out before submission.

3. **Validation**
    - On blur, validate the input field. If invalid:
        - Apply a red border and error icon to the input.
        - Display a validation message below the field.
    - On focus, clear the validation message and reset the input styling.

4. **Button Enablement**
    - The **Register** button should remain disabled until all fields are correctly filled.

5. **Registration Process**
    - On clicking the **Register** button, send a [request](https://vsqsnqnxkh.execute-api.eu-central-1.amazonaws.com/prod/docs#/default/post_auth_register) 
   to the back-end to register the user.

6. **Error Handling**
    - If registration fails, display an error message below the form based on back-end response.

## Evaluating Criteria

The maximum score for this task is **450 points**, distributed as follows:

1. **Technical Implementation (30 points)**
    - TypeScript integration (10 points)
    - Proper ESLint and Webpack/Vite configuration (5 points)
    - Adherence to strict typing rules (5 points)
    - Interfaces, enums, and generics usage (5 points)
    - Linting rules compliance (5 points)

2. **Header (30 points)**
    - User icon functionality (15 points)
    - Popup menu for non-logged-in users (7 points)
    - Popup menu for logged-in users (8 points)
   
3. **Main Page (40 points)**
    - Back-end integration and data fetching (10 points)
    - Loader implementation (10 points)
    - Error handling (10 points)
    - Slider functionality (10 points)

4. **Zoos Page (60 points)**
    - Back-end integration and data fetching (15 points)
    - Loader implementation (10 points)
    - Error handling (10 points)
    - Side menu generation (15 points)
    - Updating Did you know? section depending on the selected menu items (10 points)

5. **Did you know? section (70 points)**
    - Back-end integration and data fetching (10 points)
    - Section generation (15 points)
    - Loader implementation (10 points)
    - Error handling (10 points)
    - Modal window functionality (25 points)

6. **Make your donation popup (150 points)**
    - Step 1 functionality and validation (40 points)
    - Step 2 functionality and validation (50 points)
    - Step 3 functionality and validation (40 points)
    - Complete donation notification (20 points)
   
7. **Sign In Page (30 points)**
    - Input fields and validation (10 points)
    - Button enablement (5 points)
    - Authentication process (10 points)
    - Error handling (5 points)
   
8. **Registration Page (40 points)**
    - Input fields and validation (15 points)
    - Button enablement (5 points)
    - Registration process (15 points)
    - Error handling (5 points)



---

Enjoy coding the Online Zoos functionalities!
