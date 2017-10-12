# CS6300 SDP Fall 2017 - Group Project
by Isaac Silva (```isilva6@gatech.edu```), Mukul Pai (```mpai8@gatech.edu```) & Saad Khan (```skhan315@gatech.edu```)

# Word Scramble Game - User Manual

**Author**:  Team 47 

| Name | GT email ID |
| :-----: | :----------------- |
| Isaac Silva | ```isilva6@gatech.edu``` |
| Mukul Pai | ```mpai8@gatech.edu``` |
| Saad Khan | ```skhan315@gatech.edu``` |

**Document Tracking**: Following chart is used to log all the changes made to this document.

| Version | Date of edit/change | Who made the edit/change | Description of edit/change |
| :-----: | :-----------------: | :----------------------: | :------------------------: |
|    v1.0     |    10/13/2017                 |   Team 47                       |           *first draft*                 |

SDPCryptogram is a mobile app that allows players to practice solving cryptograms and compare their scores with others. Cryptograms are alphanumeric phrases in which the alphabetical characters are encrypted by some method, for example by shifting each character by a set number of positions in the alphabet. For each cryptogram, the player is presented with the encrypted phrase and must analyze it in order to try to discover the code and solve the puzzle. Players can submit their solutions unlimited times, but the number of incorrect submissions will be tracked and remain part their player rating along with total number of cryptograms started and solved. Administrators can add new  players to the game and new cryptograms for players to solve at any time..

## Getting Started

SDPCryptogram can be built and run on an android emulator via Android Studio. The Genymotion emulator plugin for Android Studio is recommended for better performance.

The minimum API level is 19 and the maximum is 25.

## Using SDPCryptogram

Upon launching SDPCryptogram, you will be presented with a login screen. Both administrators and players can use this screen to login, and the app will detect the type of user automatically and log them into the appropriate home screen.

A valid administrator username/password combination is **"admin"/"Password"** (without quotes). <br>
A valid player username/password combination is **"david"/"Password"** (without quotes).

Usernames and password are case-sensitive and may only contain alphanumeric characters.

The administrator home screen includes three options: **Add Player**, **Add Cryptogram**, and **Edit Cryptogram**.
* **Adding Players**: The administrator inputs each new player's first and last names, username, and password. After creation, this user information cannot be edited or changed by the administrator or the user.
* **Adding Cryptograms**: The administrator can add a cryptogram by simply providing the solution and encoded phrases. Only encoded phrases for which very alphabetic character is shifted by the same number of positions in the alphabet (Caesar cipher or shift cipher) will be allowed when creating cryptograms. Additionally, cryptograms with same solution and encoded phrases (shift by 0 positions) will not be allowed, and neither will cryptograms which include changes to non-alphabetical characters.
* **Editing Cryprograms**: The administrator can edit any previously created cryptogram at any time by inputting that cryptogram's unique ID. Changes to cryptogram phrases must adhere to the same rules outlined above for creating new cryptograms.

The player home screen includes two options: **Choose Cryptogram** and **Player Ratings**.
* **Choosing Cryptograms**: Players may select cryptograms from a list of all current cryptograms, including those started, solved, and not started. For each cryptogram in the list, a standard set of information will be displayed. The encoded phrase will be shown and will scroll horizontally if too long to display in the allotted area. To the right of the encoded phrase, the Unique ID will be shown. Below these fields will be an indicator if the player has solved the cryptogram and the number of incorrect submissions (if any). Touching a cryptogram in the list will take the player to the Solve Cryptogram screen. On this screen, the encoded phrase will be shown at the bottom and the player will be able to type in their guess at the solution phrase above it. If the player inputs any text into the solution phrase entry area and then leaves the screen without touching Solve, their progress will be saved and the cryptogram will be registered as "started." If the player is happy with their solution, they can press Solve to check it. They will receive confirmation that the solution is either correct or incorrect, and their ratings will be updated to reflect this result.
* **Viewing Player Ratings**: Players may view a list of player ratings for all remote and local players at any time. The list of player ratings will be similar in format to the list of cryptograms. For each player, their first and last name will be displayed in bold, along with their number of solved and started cryptograms as well as the total number of incorrect solutions they have submitted. Players will be ranked by total number of cryptograms solved, with the most being displayed at the top and in descending order. Touching player entries in the list will not lead to any additional information.

Navigation: Navigation in SDPCryptogram is intended to be intuitive and buttons easy to understand and use. The standard Android **Back** button can be used to navigate to previous screens when no explicit button is provided for navigation. Furthermore, the "three dot" menu symbol at the top right of every screen can be touched to display a **logout** option that will take the user back to the login page to allow switching between users.

## Built With

* [Gradle](https://gradle.org/) - Dependency Management
* [Andorid Bootstrap](https://github.com/Bearded-Hen/Android-Bootstrap) - Used for front end design

## Authors

* **Michael Amadasun** - *User Interface Software Developer*
* **Alexander Molnar** - *Application Tester*
* **Muzammil Mueen** - *Application Software Developer*
* **David Nelson** - *Application Designer/Documentation Lead*
