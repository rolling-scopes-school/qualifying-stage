# Coffee-House: Business Functionality

In this task, you are required to add business logic to the previously created layout. Here’s what you’ll be implementing:
- Interaction with the back-end
- Fetching data for the menu page and the modal window with details of the selected product
- Add a loader while waiting for the back-end response
- Error handling
- Creating **Registration** and **Sign-In** pages
- Developing a **Cart page**
- Add different views for registered and non-registered users
- Adding the functionality to **place an order**
- Communication with Local Storage

Link to the [layout](https://www.figma.com/design/vtOxEIbYsyutkVYM41ueKK/Coffee-House-v2.0?node-id=0-1&p=f&t=m8HTTyfbF7qx7t9n-0)

## Technical Requirements

1. The use of any frameworks or libraries is strictly **prohibited**.
2. **TypeScript Integration**
    - Add the **npm package TypeScript** to your application.
    - Create a `tsconfig.json` file for configuration.

2. **ESLint and Webpack/Vite Configuration**
    - ESLint should be configured to work with TypeScript.
    - Use the plugin `@typescript-eslint/recommended`.

3. **Browser Compatibility**
    - Ensure the application works in **Google Chrome**.

4. **Strict Typing**
    - All variables, function parameters, and methods should have defined types, including return types.
    - Interfaces should be actively used in the code.
    - Utilize TypeScript features such as enums, generics, and partials.

5. **Configuration File Flags**
    - Ensure the following flags are present:
        - `"noImplicitAny": true`
        - `"strict": true`

6. **ESLint Rule**
    - Enable the ESLint rule: `no-explicit-any`.

7. **Beck-end Compatibility**
   - Create all necessary interfaces to interact with the API.

## Functional Requirements

### Beck-end integration
   - Carefully review the endpoints provided by the backend and the corresponding interfaces. Use the Swagger 
documentation for this htts://6kt29kkeub.execute-api.eu-central-1.amazonaws.com/api

### Main Page
1. **Data Fetching**
    - On page load, make a [request](https://6kt29kkeub.execute-api.eu-central-1.amazonaws.com/api#/Products/ProductsController_getFavoriteProducts) to the back-end to fetch a set of 3 favorite coffee items. 

2. **Loader**
    - Show a loader while waiting for the back-end response at the location where the slider with favorite coffee examples will appear. All other page elements should be immediately available.

3. **Error Handling**
    - If an error occurs, display the text: _“Something went wrong. Please, refresh the page”_ instead of the loader.
   
5. **Slider**
    - Implement a slider that allows users to navigate through the favorite coffee items using left and right arrows.
    - The slider should loop infinitely, meaning that navigating past the last item should bring the user back to the first item, and vice versa.
    - All slider items should be programmatically generated using TypeScript and added to the page

### Menu Page
1. **Data Fetching**
    - On page load, make a [request](https://6kt29kkeub.execute-api.eu-central-1.amazonaws.com/api#/Products/ProductsController_getAllProducts) to the back-end to fetch data for the coffee cards. This includes:
        - Name,
        - Description,
        - Price,
        - Discounted price (for registered users).
    - Images. Create a folder containing all images and link them to each product using its unique ID. For images not 
   included in the design, add them manually by selecting visuals that correspond to the product name.

2. **Loader**
    - While waiting for the back-end response, display a loader.
        - The header, main title, and footer must remain immediately accessible and stick to the top and bottom of the page, respectively.

3. **Error Handling**
    - Display the text: _“Something went wrong. Please, refresh the page”_ in place of the loader in case of an error.
    - The design of the notification is entirely up to you

4. **Cards**
    - All cards should be programmatically generated using TypeScript and added to the page.
   
5. **Category Selection**: 
   - By default, only the "Coffee" category is selected, and products are filtered accordingly.
   - When another category is selected, the displayed cards should dynamically change to match the selected category.

6. **Registered Users**
    - If the user is logged in, they should see the discounted price (with the original price struck through).


### Modal Window
1. **Data Fetching**
    - When a user clicks on a product, make a back-end [request](https://6kt29kkeub.execute-api.eu-central-1.amazonaws.com/api#/Products/ProductsController_getProductById) to fetch detailed product information by its `id` and display it in a modal window.

2. **Loader**
    - While waiting for the back-end response, show an overlay with a loader.
        - The modal window should open only when the data is successfully fetched.

3. **Error Handling**
    - Display a notification at the top of the page with the text: _“Something went wrong. Please, try again”._
    - The overlay and loader should disappear.
    - The design of the notification is entirely up to you

4. **Adding to Cart**
    - Include an **“Add to Cart”** button in the modal, allowing the user to:
        - Select a size (default is the first option, only one size can be selected at a time).
          - On hover over a size, show a tooltip with the price (and, for registered users, the original price struck through and the discounted price).
        - Add extras (all or none can be selected).
          - On hover over an extra, show a tooltip with the price (and, for registered users, the original price struck through and the discounted price).
    - The total price should update dynamically based on the selected size and extras.
    - The design of the tooltip is entirely up to you

5. **Closing the Modal**
    - The modal closes upon:
        - Clicking the **“Add to Cart”** button,
        - Clicking the **close icon**, or
        - Pressing the **Esc key**.
        - Clicking outside the modal does close it.


### Cart Page
1. **Icon and Counter**
    - The cart icon should always be visible for logged-in users.
        - For non-logged-in users, it will become visible once the first item is added to the cart.
    - Display the total number of items next to the cart icon and discount in case the user is logged.

2. **Persistence**
    - Cart contents should persist even after refreshing the application until the user clears the cart manually (Local Storage).

3. **Order Details**
    - The user should see:
        - Product name,
        - Selected size,
        - Extras,
        - Price (including discounted price if available).

    - Include a **trash icon** for removing individual items. The order total should update accordingly.

4. **Authentication Prompt**
   - If the user is not logged in, show **Sign In** and **Registration** buttons below the order list, redirecting the user to the appropriate page.
   - If the user is logged in, display the delivery address and a **Confirm Order** button below the order list.
      - While the order is being placed, show a loader.
      - If an error occurs during order placement, display a not
     
5. **Checkout**
    - If the user is logged in, display the delivery address and a **Confirm Order** button below the order list.

6. **Order Confirmation**
   - When the user clicks the **Confirm Order** button make a [request](https://6kt29kkeub.execute-api.eu-central-1.amazonaws.com/api#/Orders/OrdersController_confirmOrder) to the back-end to place the order.
   - While the order is being placed, show a loader.
   - If an error occurs during order placement, display a notification at the top of the page with the text: _“Something went wrong. Please, try again”._
   - The design of the notification is entirely up to you
   - Upon successful order placement, clear the cart and display a confirmation message: _“Thank you for your order! Our manager will contact you shortly.”_


### Sign In Page
1. **Input Fields**
    - The user must input their **login** and **password**.

2. **Validation Rules**
    - **Login Rules**:
        - Must be at least 3 characters long.
        - Must start with a letter.
        - Only English alphabet letters are allowed.

    - **Password Rules**:
        - Must be at least 6 characters long.
        - Must contain at least 1 special character.

4. **Validation effects**
   - On blur, validate the input field. If invalid:
      - Apply a red border and error icon to the input.
      - Display a validation message below the field.
   - On focus, clear the validation message and reset the input styling.

3. **Button Enablement**
    - The **Sign In** button should remain disabled until both fields are correctly filled.

5. **Authentication**
    - On clicking the **Sign In** button, send a [request](https://6kt29kkeub.execute-api.eu-central-1.amazonaws.com/api#/Authentication/AuthController_login) to the back-end to authenticate the user.

5. **Error Handling**
    - If the login attempt fails, display an error message below the form: _“Incorrect login or password”_.

6. **Successful Login**
    - Upon successful login, redirect the user to the **Menu** page.

### Registration Page
1. **Input Fields and Validation**
    - **Login**:
        - At least 3 characters, start with a letter, only English letters are allowed.

    - **Password & Confirm Password**:
        - At least 6 characters and must contain at least 1 special character.
        - The two fields must match (case-sensitive).

    - **City**:
        - Dropdown with 3 cities of your choice.

    - **Street**:
        - Dropdown with 10 streets, changing dynamically based on the selected city.

    - **House Number**:
        - Numeric input field.
        - Validation: Value must be greater than 1.

    - **Payment Method**:
        - Radio buttons: `Cash` | `Card`.

2. **Mandatory Fields**
    - All fields must be filled out before submission.

3. **Validation**
    - On blur, validate the input field. If invalid:
        - Apply a red border and error icon to the input.
        - Display a validation message below the field.
    - On focus, clear the validation message and reset the input styling.
   
4. **Button Enablement**
    - The **Register** button should remain disabled until all fields are correctly filled.

5. **Registration Process**
    - On clicking the **Register** button, send a [request](https://6kt29kkeub.execute-api.eu-central-1.amazonaws.com/api#/Authentication/AuthController_register) to the back-end to register the user.

6. **Error Handling**
    - If registration fails, display an error message below the form based on beck-end response.

## Evaluating Criteria

The maximum score for this task is **360 points**, distributed as follows:

1. **Technical Implementation (30 points)**
    - TypeScript integration (10 points)
    - Proper ESLint and Webpack configuration (5 points)
    - Adherence to strict typing rules (5 points)
    - Interfaces, enums, and generics usage (5 points)
    - Linting rules compliance (5 points)

2. **Main Page (35 points)**
    - Back-end integration and data fetching (10 points)
    - Loader implementation (10 points)
    - Error handling (10 points)
    - Slider functionality (5 points)

3. **Menu Page (70 points)**
   - Back-end integration and data fetching (10 points)
   - Loader implementation (10 points)
   - Dynamic product card generation (20 points)
   - Category selection and filtering (15 points)
   - Price display logic (15 points)

4. **Modal Window (85 points)**
    - Back-end integration and data fetching (10 points)
    - Loader implementation (10 points)
    - Dynamic product card generation (20 points)
    - Error handling (10 points)
    - Add-to-Cart functionality (15 points)
    - Close modal functionality (10 points)
    - Hover effects and tooltips (10 points)

5. **Cart Page (70 points)**
    - Cart icon and item counter (20 points)
    - Persistency of cart items (15 points)
    - Proper item display and deletions (10 points)
    - Confirmation of order (10 points)
    - Error of order placement handling (15 points)

6. **Sign In Page (25 points)**
    - Input validation (10 points)
    - Enabling/disabling the button (5 points)
    - Error handling (5 points)
    - Successful login redirection (5 points)

7. **Registration Page (45 points)**
    - Correct implementation of all input fields (10 points)
    - Validation rules (20 points)
    - Enabling/disabling the button (5 points)
    - Error handling (5 points)
    - Successful registration redirection (5 points)


---

Enjoy coding the Coffee-House functionalities!
