# CS6300 SDP Fall 2017 - Assignment 5: Software Design
by Saad Khan (```skhan315@gatech.edu```)

# Word Scrabble Game

## Overview

A mixture of both data structures such as lists and variables such as string, int, boolean were utilized as part of the design. Main focus was to keep the design simple but at the same time incorporating all what was needed as per the requirements.

## Requirements

### 1. When starting the application, a user may choose to either create a new player or log in.  For simplicity, authentication is optional.  A (unique) username will be sufficient for logging in.

**Response:** The starting of the application can be realized as user, represented by User GUI, which could give 2 options to the user (new player, login) along with an empty text box to put in the user's username. If the user is an existing player, he/she would login otherwise he/she would go onto create a unique profile.

### 2. After logging in, the application shall allow players to 

#### (1) create a word scramble,

#### (2) choose and solve word scrambles,

#### (3) see statistics on their created and solved word scrambles, and

#### (4) view the player statistics.

**Response:** All of the above functionalities will be addressed within the player class.

The **createWordScramble()** method will address '(1) create a word scramble'.

The **chooseWordScramble()** method will address '(2) choose and solve word scrambles' and present the player with a list of word scrambles to choose from.

The **viewScrambleStatistics()** method will take of the scramble statistics and will return the scramble stats for that particular player.

Similarly, **viewPlayerStatistics()** method will take of the player statistics and will return the personal player stats for that particular player.

### 3. The application shall maintain an underlying database to save persistent information across runs (e.g., word scrambles, player information, statistics).

### 4. Word scrambles and statistics will be shared with other instances of the application.  An external web service utility will be used by the application to communicate with a central server to:

#### a. Add a player and ensure that their username is unique.

#### b. Send new word scrambles and receive a unique identifier for them.

#### c. Retrieve the list of scrambles, together with information on which player created each of them. 

#### d. Report a solved scramble.

#### e. Retrieve the list of players and the scrambles each have solved.

### You should represent this utility as a utility class that (1) is called "ExternalWebService", (2) is connected to the classes in the system that use it, and (3) explicitly list relevant methods used by those classes.  This class is provided by the system, so it should only contain what is specified here. You do not need to include any aspect of the server in your design besides this utility class.


### 5. When creating a new player, a user will:

#### a. Enter the player’s first name.

#### b. Enter the player’s last name.

#### c. Enter the player’s desired username.

#### d. Enter the player’s email.  

#### e. Save the information.

#### f. Receive the returned username, with possibly a number appended to it to ensure that it is unique.

### 6. To add a word scramble, the player will:

#### a. Enter a phrase (not scrambled).

#### b. Enter a clue. 

#### c. View the phrase scrambled by the system. If the player does not like the result, they may choose for the system to re-scramble it until they are satisfied.

#### d. Accept the results or return to previous steps.

#### e. View the returned unique identifier for the word scramble. The scramble may not be further edited after this point.

### 7. A scramble shall only mix up alphabetic characters, keeping each word together. Words are contiguous sequences of alphabetic characters separated by one or more non-alphabetic characters.

### 8. All other characters and spacing will remain as they originally are.

### 9. When solving word scrambles, a player will:

#### a. View the list of unsolved word scrambles, by identifier, with any in progress scrambles marked and shown first.

#### b. Choose one word scramble to work on.

#### c. View the scramble.

#### d. Enter the letters in a different order to try to solve the scramble.

#### e. Submit a solution.

#### f. View whether it was correct.

#### g. Return either to the puzzle, if wrong, or to the list, if correct.

### 10. A player may exit any scramble in progress at any time and return to it later.  The last state of the puzzle will be preserved.

### 11. The scramble statistics shall list all scrambles with

#### (1) their unique identifier,

#### (2) information on whether they were solved or created by the player, and

#### (3) the number of times any player has solved them. This list shall be sorted by decreasing number of solutions.

### 12. The player statistics will list players’ first names and last names, with

#### (1) the number of scrambles that the player has solved,

#### (2) the number of new scrambles created, and

#### (3) the average number of times that the scrambles they created have been solved by other players.  It will be sorted by decreasing number of scrambles that the player has solved.

### 13. The User Interface (UI) shall be intuitive and responsive.
