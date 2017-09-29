1 - When starting the application, a user may choose to either create a new player or log in.  For simplicity, authentication is optional.  A (unique) username will be sufficient for logging in.

To realize this requirement, I added a class "User" to represent the player, with an attribute "username". A method signature was added to the same class:

- login(username: String): Boolean

That method returns true or false depending if the user logged in or not.


2 - After logging in, the application shall allow players to  (1) create a word scramble, (2) choose and solve word scrambles, (3) see statistics on their created and solved word scrambles, and (4) view the player statistics.

Even though this is more an UI requirement, it helped me understand some of the other elements of the domain. Thus, I added a class "Game" to be used as a blueprint for the creation of word scrambles and an association class "PlayEvent" for the actual action of a user playing a particular game instance. 


3 - The application shall maintain an underlying database to save persistent information across runs (e.g., word scrambles, player information, statistics).

I did not consider this requirement because the database does not affect the design directly.

4 - Word scrambles and statistics will be shared with other instances of the application.  An external web service utility will be used by the application to communicate with a central server to:

a - Add a player and ensure that their username is unique.
b - Send new word scrambles and receive a unique identifier for them.
c - Retrieve the list of scrambles, together with information on which player created each of them. 
d - Report a solved scramble.
e - Retrieve the list of players and the scrambles each have solved.


In order to realize this requirement, added an Utility class called "ExternalWebService" with the following methods in order to fulfill each of the above-described functionalities:

a - addUser(username: String): String 
b - addNewWordScrambleGame(game: Game): Integer
c - getListOfWordScrambleGamesAndAuthors(): ArrayList<Map<Game, User>>
d - reportSolvedScramble(game: Game)
e - retrievePlayersAndSolvedScrambles: ArrayList<Map<User, ArrayList< Game>>>
 

A few remarks on the steps to fulfill this requirement:

- Added unique identifier as a property in the Game class, according to indications of the "b" requirement.
- The addUser method returns an unique username as a String


5 - When creating a new player, a user will:

a - Enter the player’s first name.
b - Enter the player’s last name.
c - Enter the player’s desired username.
d - Enter the player’s email.  
e - Save the information.
f - Receive the returned username, with possibly a number appended to it to ensure that it is unique.

In order to realize this requirement, I added the following properties to the User class:

firstName: String
lastName: String
desiredUsername: String
username: String
email: String

The following methods were added:

- createNewPlayer(firstName, lastName, desiredUsername, email): String

The above method returns a username that the system registered by using the ExternalWebService utility class. The addUser method signature was changed to address that requirement and became as follows:

- addUser(firstName, lastName, desiredUsername, email): String

That method returns a player's username that the remote system assigned to the user. 


6 - To add a word scramble, the player will:

a - Enter a phrase (not scrambled).
b - Enter a clue. 
c - View the phrase scrambled by the system. If the player does not like the result, they may choose for the system to re-scramble it until they are satisfied.
d - Accept the results or return to previous steps.
e - View the returned unique identifier for the word scramble. The scramble may not be further edited after this point.


In order to realize this requirement, the following property fields were added to the Game class:

identifier: Integer
originalPhrase: String
clue: String
scrambledPhrase: String

The following methods were added to the Game class:

- createNewGame(phrase: String, clue: String): Integer
- refreshScrambledPhrase()
- saveGame(): Integer

A few remarks on the steps to fulfill this requirement:

- The createNewGame method saves the game object locally until the user accepts the scrambled phrase
- The refreshCrumbledPhrase method fulfills requirement "C" above
- The saveGame method saves the game and returns the final identifier
- The saveGame method uses the ExternalWebService utility class. More specifically the "addNewWordScrambleGame(game: Game): Integer" method signature


7 - A scramble shall only mix up alphabetic characters, keeping each word together. Words are contiguous sequences of alphabetic characters separated by one or more non-alphabetic characters.

In order to realize this requirement, the scrumbledPhrase property on the Game class was confirmed to be "String"

8 - All other characters and spacing will remain as they originally are.

This requirement does not affect the UML design

9 - When solving word scrambles, a player will:

a - View the list of unsolved word scrambles, by identifier, with any in progress scrambles marked and shown first.
b - Choose one word scramble to work on.
c - View the scramble.
d - Enter the letters in a different order to try to solve the scramble.
e - Submit a solution.
f - View whether it was correct.
g - Return either to the puzzle, if wrong, or to the list, if correct.


In order to realize this requirement, the following steps were taken:

- In order to fulfill requirement "a", the method "retrievePlayersAndSolvedScrambles: ArrayList<Map<User, ArrayList< Game>>>" available in the ExternalWebService utility class is used to filter the results of the "getListOfWordScrambleGamesAndAuthors(): ArrayList<Map<Game, User>>" method, also available the same utility class. This gives a list of unsolved word scrambles for a particular user. To show the scrambles in progress for a user, a method called "getInProgressGameList(): List<Game>" was added to the User class. The list returned by this method is used in combination with the list returned and filtered by the mentioned utility methods.
- A method signature "submitSolution(solution: String): Boolean" was added. If the solution is correct the method returns true, otherwise it returns false.
- If the solution is correct call the method "reportSolvedScramble(game: Game)", available in the ExternalWebService utility class.


10 - A player may exit any scramble in progress at any time and return to it later.  The last state of the puzzle will be preserved.

In order to fulfill this requirement a property called "gameState" was added to the PlayEvent class. In addition, the following method signature was added to the same class:

- updateGameState(state: String)

This method assumes the game state is in a string format.


11 - The scramble statistics shall list all scrambles with (1) their unique identifier, (2) information on whether they were solved or created by the player, and (3) the number of times any player has solved them. This list shall be sorted by decreasing number of solutions.

In order to realize this requirement, two methods are used from the ExternalWebService utility class:

- retrievePlayersAndSolvedScrambles: ArrayList<Map<User, ArrayList< Game>>>
- getListOfWordScrambleGamesAndAuthors(): ArrayList<Map<Game, User>>

The former returns a list of all players and the scrambles each solved. The latter returns the list of all scrambles and its authors. By callind both methods, filtering the results and making the appropriate calculations, we get fulfill the requirements described in this section. For convenience, we also added a new property called "numberOfTimesSolved: Integer" in the Game class, in order to facilitate sorting of games by the number of times players solved them. A setter method called "setSolvedTimes(game: Game)" was added to the same class in order to set the numberOfTimesSolved attribute.


A method called "getScrambleStatistics()" was added to the Game clas in order to wrap the calls to the methods in the ExternalWebService utility class and perform the necessary filtering and calculations. 


12 - The player statistics will list players’ first names and last names, with (1) the number of scrambles that the player has solved, (2) the number of new scrambles created, and (3) the average number of times that the scrambles they created have been solved by other players.  It will be sorted by decreasing number of scrambles that the player has solved.

In order to realize this requirement, two methods are used from the ExternalWebService utility class:

- retrievePlayersAndSolvedScrambles: ArrayList<Map<User, ArrayList< Game>>>
- getListOfWordScrambleGamesAndAuthors(): ArrayList<Map<Game, User>>

By callind the above methods, filtering the results and performing the necessary calculations accordingly, points 1,2,3 can be easily met. In order to facilitate sorting and making the calculations more explicit, the following properties, alongside with its setters methods, were added to the User class:

- numberOfSolvedGames: Integer
- numberOfGamesCreated: Integer 
- authoredGamesSolvedAverage: Integer


A method called "getPlayerStatistics()" was added to the User class in order to wrap the calls to the methods in the ExternalWebService utility class and perform the necessary filtering and calculations. 


13 - The User Interface (UI) shall be intuitive and responsive.

This requirement does not affect the UML design
 
