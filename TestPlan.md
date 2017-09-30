# Test Plan 

**Version**: 3.0 *(Updated with complete test results)*<br>
**Author**: Team 25

## 1 Testing Strategy

### 1.1 Overall strategy

Our overall testing strategy goal is to have a clear understanding of why each part of our software either works or does not work throughout the entire developmental process. In order to achieve this goal, we will utilize a series of instrument system tests to validate the overall functionality of each piece of our software at any given time. This will be crucial in allowing us to identify areas to focus our efforts and keep the developmental process moving forward smoothly and efficiently.

The tests for each piece of software will ensure the basic building blocks of our program first run correctly in isolation. Once we have multiple pieces of code working correctly, we will utilize integration testing to observe how they interact together and validate their effectiveness. For example, we will have tests that just check login and then others that check player creation and then login. This will allow us to ensure that, though each individual block of code works in isolation, they are also providing the correct inputs and outputs to each other and completing the overall process. As we continue to perform testing while our software builds, we will also begin to utilize regression testing strategies. Regression testing is a way to look back and retest pieces of code previously validated to ensure that software updates and changes have not altered their function. Regression testing is an ongoing strategy that will continue throughout the entire developmental process. Finally, system testing involves the overall functionality of the finished software to ensure that it is meeting all requirements. Any errors in system testing will help us reach back into the other testing levels and identify which areas need improvement.

Developing test cases will be a collaborative effort including all members of the team. Testing will require the input and thought of all team members because each individual will be able to provide insight into the requirements of different pieces of the software. One team member will complete the espresso tests to be checked off by other team members.

### 1.2 Test Selection

Team 25 will utilize a mixture of tests to achieve the strategy and developmental goals listed above. 
We will utilize black-box testing in order to ensure that the blocks of code are creating the correct output for a large sample of our expected inputs. We will use Junit testing framework to develop these test cases. Black-box testing techniques will allow us to cover a large range of functionality. Then, if an issue is identified, we can focus in on that error to identify the exact area of code causing the issue. 

### 1.3 Adequacy Criterion

In order to assess the quality of our test cases we will ensure we are achieving between
80-90% coverage of all the code's functionality. Though this does not mean we have necessarily
identified every single error in the code, aiming for 80-90% structural and functional coverage
will help us better understand the code and minimize as many errors as possible.

### 1.4 Bug Tracking

We will utilize the open-source software Bugzilla to manage our bugs and enhancement requests
throughout the developmental process. It a clear and easy to use tool that the entire
team can utilize in order to efficiently keep track of issues and progress.

### 1.5 Technology

Team25 will use JUnit as its testing technology. It is a testing framework specifically
designed for Java and is the tool the team is most familiar with. We will utilize the Android Studio Esperesso Test tool in order to develop a set of automated tests for functionality of the application.

## 2 Test Cases

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

![Test Screenshot](images/TestScreenShot.PNG)
