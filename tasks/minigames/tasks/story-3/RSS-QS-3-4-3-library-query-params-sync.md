# Task RSS-QS-3-4-3: Library Query Parameters Synchronization & Data Not Found Banner (40 points)

## Description

Synchronize Library page interactive controls (category filter chips, sort order dropdown, pagination) with URL query parameters, support deep-linking and browser history navigation, and display a "Data Not Found" banner with a reset action when API queries return empty datasets.

## Acceptance Criteria

- **URL Query String Synchronization:** Interactive Library page states should be continuously reflected in URL query parameters. Example:
  - Filter category: `category=<category-name>`
  - Sort order: `sort=<sort-field>`
  - Page number: `page=<page-number>`
  - *Full Query Example:* `/library?category=action&sort=rating-desc&page=2`
- **Single Source of Truth with API:** Filter, sort, and pagination changes update the URL and trigger the corresponding backend API request. Deep links restore UI controls and fetch matching API data.
- **Non-Reload URL Updates:** Selecting a category filter chip, changing the sort dropdown value, or clicking pagination buttons updates the URL query string in the browser address bar dynamically without full page reloads.
- **Deep Link State Restoration:** Copying a Library page URL with query parameters and opening it in a new tab or window immediately restores the exact UI state (active category chip highlight, selected sort option, page number) and triggers the corresponding backend API request.
- **Browser History Integration:** Navigating via browser Back/Forward controls updates the URL query string and updates the Library filter/sort/pagination UI state and card list.
- **Data Not Found Banner for Library:** If invalid/erroneous query parameters are used or if the backend API returns an empty list of games for the selected filter/sort/pagination criteria:
  - A prominent banner/card should be rendered inside the game card list container stating that no data was found for the selected criteria.
  - The banner should contain a clear button (e.g. "Reset Filters") that resets the category filter, sort option, and pagination back to default states (`All Games`, default sorting, `page=1`) and updates the URL parameters.
  *The visual layout and styling of the Data Not Found banner are at the student's discretion.*
