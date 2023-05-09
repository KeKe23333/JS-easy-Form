# 简单的JS练习，Form表单

# Assessment 2 - FunForm

## Change Log

## Tasks

### Task 1 - Dynamic form

The page `task1/page.png` displays a series of inputs, and when valid, outputs a "summary" of this information in the textarea at the bottom of the page.

![](./task1/page.PNG)

No CSS is required in this task. Please do not worry about styling your pages.

#### The page  页面中包含以下元素
 * Table
   * Text input for `Street` Name (must be between 3 and 50 characters).
   * Text input for `Suburb` (must be between 3 and 50 characters).
   * Text input for `Postcode` (must be a number that is exactly 4 digits).
   * Text input for `Date of birth` (valid input is the exactformat "DD/MM/YYYY" and must be a valid date. This means it must match the regex expression "[0-9]{2}/[0-9]{2}/[0-9]{4}" and when trying to parse it with the Javascript date object it does not return **NaN**).
   * Dropdown for `building type` (either "Apartment" or "House", no other options). Apartment is default.
   * Checkbox for `features` that the house has (Heating, AirConditioning, Pool, Sandpit).
   * Button to select / deselect all.
 * Remove button
 * Textarea (initially blank)

#### Actions 以下是触发渲染的事件，这些事件应该绑定到特定的操作

The following are events that trigger a render that should be binded to particular actions
* Changing of the "building type" or "features" should trigger a render.
* Blur of the "street name", "suburb", "postcode", or "date of birth" should trigger a render.

There are key buttons on the page:
* When the `Select All` button is clicked inside the features section, all 4 feature checkboxes are selected.
  * At any time when all 4 features are selected, the `Select All` button's text is changed to `Deselect all`. When this button is pressed in this state, all 4 of the feature checkboxes become unselected.
* When the `reset` button is clicked, the `textarea` has all of its text removed (i.e. it becomes blank again), and all of the form elements in the table are reset to their default state
