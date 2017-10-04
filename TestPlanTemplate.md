
# Test Plan

<!--*This is the template for your test plan. The parts in italics are concise explanations of what should go in the corresponding sections and should not appear in the final document.*-->

**Author**:  Team 47 

| Name | GT email ID |
| :-----: | :----------------- |
| Isaac Silva | ```isilva6@gatech.edu``` |
| Mukul Pai | ```mpai8@gatech.edu``` |
| Saad Khan | ```skhan315@gatech.edu``` |

**Document Tracking**: Following chart is used to log all the changes made to this document.

| Version | Date of edit/change | Who made the edit/change | Description of edit/change |
| :-----: | :-----------------: | :----------------------: | :------------------------: |
|    v1.0     |    10/04/2017                 |   Team 47                       |           *first draft*                 |

## 1 Testing Strategy

### 1.1 Overall strategy

<!--*This section should provide details about your unit-, integration-, system-, and regression-testing strategies. In particular, it should discuss which activities you will perform as part of your testing process, and who will perform such activities.*-->



Our overriding goal to test the strategy is to have a clear understanding of why each part of our software is working or not working through the entire development process. To achieve this goal, we use a series of tests of the instrumentation system to validate the general functionality of each piece of our software at any time. This will be crucial in identifying areas to focus our efforts and keep the development process running smoothly and efficiently.

Our overall testing strategy goal is to have a clear understanding of why each part of our software either works or does not work throughout the entire developmental process. In order to achieve this goal, we will utilize a series of instrument system tests to validate the overall functionality of each piece of our software at any given time. This will be crucial in allowing us to identify areas to focus our efforts and keep the developmental process moving forward smoothly and efficiently.

The tests for each piece of software will ensure the basic building blocks of our program first run correctly in isolation. Once we have multiple pieces of code working correctly, we will utilize integration testing to observe how they interact together and validate their effectiveness. For example, we will have tests that just check login and then others that check player creation and then login. This will allow us to ensure that, though each individual block of code works in isolation, they are also providing the correct inputs and outputs to each other and completing the overall process. As we continue to perform testing while our software builds, we will also begin to utilize regression testing strategies. Regression testing is a way to look back and retest pieces of code previously validated to ensure that software updates and changes have not altered their function. Regression testing is an ongoing strategy that will continue throughout the entire developmental process. Finally, system testing involves the overall functionality of the finished software to ensure that it is meeting all requirements. Any errors in system testing will help us reach back into the other testing levels and identify which areas need improvement.

Developing test cases will be a collaborative effort including all members of the team. Testing will require the input and thought of all team members because each individual will be able to provide insight into the requirements of different pieces of the software. One team member will complete the espresso tests to be checked off by other team members.


    Establish test objectives
    Design criteria: correctness, feasibility, coverage, functionality
    Write test cases
    Testing test cases
    Execute test cases
    Evaluate test results

Unit Testing

    Interfaces tested for proper information flow
    Boundary conditions, error paths tested

Integration Testing

    Top down: have main program as driver and use stubs for components; test as components are developed and integrated
    Bottom up: components are combined into functional clusters and tested

System Testing

    Recovery testing: find failure scenarios and handle them
    Security testing: can GroceryList or ItemDatabase information be illegally modified
    Stress testing: test limits - number of items, lists
    Performance testing: test search, modify, delete times; how long it takes to perform actions

Regression Testing

    With full set of test cases, testing can be separated into Manual and Automated
    Automation framework for functional testing
    Manual testers to run remaining test cases
    Results will be compared with expected to catch SW defects from SW changes
    Report for each new build


### 1.2 Test Selection

*<!--Here you should discuss how you are going to select your test cases, that is, which black-box and/or white-box techniques you will use. If you plan to use different techniques at different testing levels (e.g., unit and system), you should clarify that.*-->

Team 47 will utilize a mixture of tests to achieve the strategy and developmental goals listed above. 
We will utilize black-box testing in order to ensure that the blocks of code are creating the correct output for a large sample of our expected inputs. We will use Junit testing framework to develop these test cases. Black-box testing techniques will allow us to cover a large range of functionality. Then, if an issue is identified, we can focus in on that error to identify the exact area of code causing the issue. 

Test cases used will be initially drawn from use cases.

### 1.3 Adequacy Criterion

<!--*Define how you are going to assess the quality of your test cases. Typically, this involves some form of functional or structural coverage. If you plan to use different techniques at different testing levels (e.g., unit and system), you should clarify that.*-->


In order to assess the quality of our test cases we will ensure we are achieving between
80-90% coverage of all the code's functionality. Though this does not mean we have necessarily
identified every single error in the code, aiming for 80-90% structural and functional coverage
will help us better understand the code and minimize as many errors as possible.

Adequacy will be measured by how well the following questions are answered:

    Are we building the product right (verification)?
    Are we building the right product (validation)?


### 1.4 Bug Tracking

<!--*Describe how bugs and enhancement requests will be tracked.*-->

We will utilize the open-source software Bugzilla to manage our bugs and enhancement requests
throughout the developmental process. It a clear and easy to use tool that the entire
team can utilize in order to efficiently keep track of issues and progress.

Will use JIRA, a bug tracking product. Any issues will be filed with: title, build version, description, steps to reproduce, with attached pic/videos as deemed necessary. In addition, priority and the developer who owns the feature will be assigned.

### 1.5 Technology

<!--*Describe any testing technology you intend to use or build (e.g., JUnit, Selenium).*-->

Team47 will use JUnit as its testing technology. It is a testing framework specifically
designed for Java and is the tool the team is most familiar with. We will utilize the Android Studio Esperesso Test tool in order to develop a set of automated tests for functionality of the application.

For automation testing, JUnit and Espresso will be used to simulate the test cases.

JUnit is a unit testing framework for Java. Espresso is a UI test framework used to create automated UI tests for and Android app.

## 2 Test Cases

<!--*This section should be the core of this document. You should provide a table of test cases, one per row. For each test case, the table should provide its purpose, the steps necessary to perform the test, the expected result, the actual result (to be filled later), pass/fail information (to be filled later), and any additional information you think is relevant.*-->


| **ID** | **Purpose** | **Steps** | **Expected** | **Actual** | **Pass/Fail** |   **Other** |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Test login Player | User logs into alex Player with (alex, Password) | Successful log in message | Successful login message | Pass | Automatic |
| 2 | Test login Player | User logs into michael Player with (michael, Password) | Successful log in message | Successful login message | Pass |  Automatic |
| 3 | Test login Admin | User logs into admin with (admin, Password) | Successful log in message | Successful login message | Pass |  Automatic |
| 4 | Test login failed | User enters invalid Admin username and password (dog, cat) | Error log in message | Failure log in message | Pass |  Automatic |
| 5 | Player selects cryptogram from choose cryptogram menu | Player is provided list of cryptograms and selects one | Successful selection | Successful selection | Pass  | Automatic  |
| 6 | Player views player ratings menu | Player is provided list of player ratings | Player Ratings displayed | Player Ratings displayed | Pass | Automatic  |
| 7 | Player logs out | Player logs out of account | Return to login menu | Return to login menu | Pass | Automatic  |
| 8 | Admin logs out | Admin logs out of account | Return to login menu | Return to login menu | Pass | Automatic  |
| 9 | Admin adds player correctly | Admin adds first name, last name, password, and username | Player is added | Player added  | Pass  |Automatic   |
| 10 | Admin adds player incorrectly | Admin inputs incorrect values for player | Player is rejected | Player is rejected| Pass  | Automatic |
| 11 | Admin adds cryptogram correctly | Admin adds solution phrase, encoded phrase, and saves cryptogram | Cryptogram is added | Cryptogram is added  | Pass | Automatic  |
| 12 | Admin adds cryptogram incorrectly | Admin inputs incorrect values for cryptogram | Cryptogram is rejected | Cryptogram is rejected | Pass  | Automatic  |
| 13 | Admin attempts to edit cryptogram that does not exist | Admin clicks on edit cryptogram and types in invalid ID | Error message | Error message  | Pass  | Automatic   |
| 14 | Add Player and Log in | Admin adds player, logs out, user logs in as new player | New player created and logged in | New player created and logged in | Pass | Automatic |
| 15 | Special Character Add | Admin clicks add cryptogram, puts in (solution: ab;c encoded: bc;d) | Cryptogram accepted | Cryptogram accepted | Pass | Automatic |
| 16 | Add player with numbers | Admin adds player with characters and numbers | Player created | Player created | Pass | Automatic |
| 1m | Admin adds cryptogram then edits it | Admin creates cryptogram with (solution: def, encoded: efg), edits it to (solution: defg, encoded: efgh) | cryptogram is edited | cryptogram is edited | pass | Manual |
| 2m | Player Correctly solves cryptogram | Player provides correct solution | Solution is accepted | Solution is accepted  | Pass  |  Manual |
| 3m | Player Incorrectly solves cryptogram | Player provides incorrect solution | Solution is rejected | Solution is accepted  |  Pass | Manual  |

**Note**: Trying to run automated tests with third-party emulator plugins such as Genymotion may cause some to fail due to lack of support of some features. All tests should pass when using the emulator included with Android Studio. The below image is a screenshot of all automated tests (16) showing as passed.

###Grocery List Manager

Grocery List Manager Test Pre-conditions: 
- App is open to default page which is an empty grocery list

|Purpose       |Steps                                                  |Expected Result            |Actual Result|P/F info|Other|
|:-------------|:-----------------------------------------------------:|:--------------------------|:------------|:-------|:----|
|1. Create Grocery List |Press "add" menu item, populate pop-up name field, press OK  |Grocery List with name created, updated in UI| Grocery List with name created, updated in UI| Pass| |
|2. Rename Grocery List |Press "edit name" menu item for selected Grocery List, modify the name field, press OK |Selected Grocery List is renamed, shown in UI |Selected Grocery List is renamed, shown in UI|Pass||
|3. Delete Selected Grocery List(s) |Press "delete selected" menu item for selected grocery list(s), pop-up to confirm |Selected Grocery List is removed, not in UI |Selected Grocery List is removed, not in UI |Pass||
|4. Delete Selected Grocery List (Empty List Selected) |Press "delete selected" menu item for no selected grocery list, pop-up to confirm  |Error message pops-up, User is taken back to Grocery Manaager screen with no update  |Error message pops-up, User is taken back to Grocery Manaager screen with no update   |Pass||
|5. Delete All Grocery List |Press "delete all" menu item for grocery list, pop-up to confirm |All Grocery List(s) is removed, not in UI |All Grocery List is removed, not in UI |Pass||
|6. Select Grocery List |Press on the Grocery List|Grocery List is selected, the Grocery List screen for that list is shown in UI |Grocery List is selected, the Grocery List screen for that list is shown in UI|Pass||

*Cancel button for above cases will return to initial test pre-condition state

###Grocery List

Grocery List Test preconditions: 
- App is open with the default page which has two grocery lists with no items

|Purpose       |Steps                                                  |Expected Result            |Actual Result|P/F info|Other|
|:-------------|:-----------------------------------------------------:|:--------------------------|:------------|:-------|:----|
|7. Add Item from dropdown| Press the "add by type" menu item, click on desired item type, item name and type in desired quantity, press OK button to confirm|Item is successfully added to Grocery List, updated in UI |Item is successfully added to Grocery List, updated in UI |Pass||
|8a. Add Item from search |Press the "search" menu item, type in item, press search button, results will populate, user selects the desired item| Item is successfully added to Grocery List, updated in UI|Item is successfully added to Grocery List, updated in UI|Pass||
|8b. Add new Item from search (successful)|If no results from 8a, pop-up with proposed item name, unit field, quantity and item type will ask the user to populate the fields and if they want to add the item to the database. User adds valid input and confirms. |Item is successfully added to Grocery List, updated in UI|Item is successfully added to Grocery List, updated in UI|Pass||
|9. Delete Selected Item(s) | Press the "delete selected" menu item for selected item(s), press OK button on pop-up to confirm |Selected item is removed from the Grocery List screen | Selected item is removed from the Grocery List screen|Pass||
|10. Delete All Item | Press the "delete all" menu item, press OK button on pop-up to confirm |All Item(s) is removed from the Grocery List screen |All Item(s) is removed from the Grocery List screen |Pass||
|11a. Update Item (valid) | Press the item you want to update the quantity, pop-up with quantity shows up, update the field and confirm |Item quantity is updated in the Grocery List screen|Item quantity is updated in the Grocery List screen|Pass||
|11b. Update Item (invalid)| Press the item you wnat to update the quantity, pop-up with quantity shows up, update the field with invalid (non-int) value and confirm | Error message pops-up, User is taken back to Grocery List screen with no update |Error message pops-up, User is taken back to Grocery List screen with no update|Pass||

*Cancel button for above cases will return to initial test pre-condition state

|Purpose       |Steps                                                  |Expected Result            |Actual Result|P/F info|Other|
|:-------------|:-----------------------------------------------------:|:--------------------------|:------------|:-------|:----|
|12. Check Item | Press the checkbox next to the item | The Item checked attribute and UI is updated |The Item checked attribute and UI is updated|Pass||
|13. Check All Items | Press the All Items checkbox (initially blank) | All items checked attribute are True and UI is updated |All items checked attribute are True and UI is updated|Pass||
|14. Clear All Items | Press the All Items checkbox (initially checked) | All items checked attribute are False and UI is updated |All items checked attribute are False and UI is updated|Pass||
|15. Back Button | Press the back button, user is taken to Grocery List Manager Screen |The Grocery List Manager screen is on display on the UI |The Grocery List Manager screen is on display on the UI|Pass||
