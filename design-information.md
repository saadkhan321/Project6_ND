# Software Design – Cryptogram Game

# Basic Design Criteria &amp; Thought process

As a seasoned programmer, I tried my best to use data structures wherever I could, rather than basic variable types. Variable types like strings and integers were used where we needed a simple functionality. For cases where we needed lists, I made data structures specific to usage.

# Classes

A brief description of classes that I used:

## Player

The class for player. Contains all the functionality which a single player can perform

## Administrator

Holds the functions of what administrator can do

## Cryptogram

Holds the attributes of a cryptograms. Saved as is in the database

## ExtraWebServer

The &#39;blackbox&#39; (as mentioned in office hours) for functionality associated with external web server.

## Players rating list

Data structure to hold the list of player ratings fetched via ExternalWebService.

## CryptogramList

Data Structure to hold the list of cryptograms from database.

## SolveCryptogram

The association class for solving cryptogram

## addCryptogram

Association class for adding a new cryptogram

## Database

The database object, holding persistent values

# Requirements Analysis &amp; Implementation

Req 1. A user shall be able to choose to log in as the _administrator_ or as a specific _player_ when starting the application.  For simplicity, authentication is optional.

**ANS:**  In my design, this point is related to point 13 of GUI, which would present the option to login as player or as an administrator. As we are not presenting GUI in this design, this requirement is realized by two classes &#39;Player&#39; &amp; &#39;Administrator&#39;.

Req 2. The application shall allow _players_ to  (1) choose a cryptogram to solve, (2) solve cryptograms, (3) see previously solved cryptograms, and (4) view the list of player ratings.

**ANS:**  This requirement is realized by the native functions of player class. Player class holds the information of how many games a particular player has played, and how many times he has been successful &amp; unsuccessful. This information along with the listCryptogram() function can easily present a comprehensive list which covers point 1 &amp; 3.

Point 2 is realized with solveCryptogram functionality.

Point 4 is realized by &#39;using&#39; the ExtraWebService functionality via Player&#39;s native function of ListPlayerRatings().

Req 3. The application shall allow the _administrator_ to (1) add new cryptograms, and (2) add new local players.

**ANS:**  These requirements are realized by functionality in &#39;Administrator&#39; class. The &#39;addPlayer&#39; function can add a plyer. The &#39;addCryptogram()&#39; functionality can address point 2.

Req 4. The application shall maintain an underlying database to save persistent information across runs (e.g., cryptograms, players, solutions).

**ANS:**  This requirement is realized by a blackbox object of Database.

Req 5. Cryptograms and player ratings will be shared with other instances of the application.  An _external web service utility_ will be used by the application to communicate with a central server to:
  1. Send updated player ratings.
  2. Send new cryptograms and receive a unique identifier for them.
  3. Request a list of additional cryptograms.
  4. Request the current player ratings.

You should represent this utility as a [utility class](http://www.uml-diagrams.org/class-reference.html) called &quot;_ExternalWebService_&quot; that (1) is connected to the other classes in the system that use it and (2) explicitly lists relevant methods used by those classes.

**ANS:**  This requirement is realized by the so called &#39;black box&#39; utility class of &#39;ExternalWebService&#39; which has all the 4 functions a – d defined explicitly This class is used by both cryptogram and Player class.

Req 6. A cryptogram shall have an encoded phrase (encoded with a simple substitution cipher), and a solution.

**ANS:**  This requirement is realized by the attributes in cryptogram class which has both encoded phrase and the solution, both of type string.

Req 7. A cryptogram shall only encode alphabetic characters, but it may include other characters (such as punctuation, numbers, or white spaces).

**ANS:**  To me this requirement is minor as compared to the overall design of the system and hence it should be handled by the &#39;addCryptogram&#39; function in Administrator class.

Req 8. To add a player, the administrator will enter the following player information:
  1. A first name
  2. A last name
  3. A unique username

**ANS:**  This functionality is handled by the &#39;addPlayer&#39; function of Administrator, which performs the function on Player class.

Req 9. To add a new cryptogram, an administrator will:
  1. Enter a solution phrase.
  2. Enter a matching encoded phrase.
  3. Edit any of the above information as necessary.
  4. Save the complete cryptogram.

After doing so, the administrator shall see a confirmation message. The message shall contain the unique identifier assigned to the cryptogram by the _external web service utility_.

**ANS:**  New cryptograms can be added by administrator using the addCryptogram function, while providing req a, b. The result of the function is handled by the Boolean value of &#39;isSuccessful&#39; to show if the process was successful, and the returned uniqueIdentifier by &#39;Cryptogram&#39; class, which uses ExternalWebService to get this identifier.

For point c, I think of it as a requirement if admin needs to edit any cryptogram, so I added a function called &#39;editCryptogram&#39; to handle it.

Point d will be handled internally by both addCryptogram and editCryptogram.

Req 10. To choose and solve a cryptogram, a player will:
  1. Choose a cryptogram from a list of all available cryptograms (see also Requirement 11).
  2. View the chosen cryptogram (including any prior solution, complete or in progress, in case he or she already worked on the same cryptogram earlier).
  3. Assign (or reassign) replacement letters to the encrypted letters and view the effects of these assignments in terms of resulting potential solution.
  4. Submit the current solution when he or she has replaced all letters in the puzzle and is satisfied with such solution.

At this point, the player shall get a result indicating whether the solution was correct. At any point, the player may return to the list of cryptograms to try another one.

**ANS:**  Point a can be achieved by the listCryptogram function of &#39;Player&#39; class. This function will further process its internal attributes like CorrectSolved, IncorrectSolved to make a complete list. This same function will also address point b. For point c &amp; d, the solveCryptogram function will be used. Player will make a solution and communicate it to &#39;cryptogram&#39; class which holds both the string and answer. The Boolean value of answerCorrect shows if the solution is ok or not.

Req 11. The list of available cryptograms shall show, for each cryptogram, its identifier, whether the player has solved it, and the number of incorrect solution submissions, if any.

**ANS:**  The is handled by the data structure &#39;CryptogramList&#39;. It&#39;s a collection of objects pulled from database as required. The cryptogram ids are pulled from database and the other information is filled using native attributes of &#39;CorrectlySolved&#39; &amp; &quot;IncorrectlySolved&quot; in Players class.

Req 12. The list of player ratings shall display, for each player, his or her name, the number of cryptograms solved, the number of cryptograms started, and the total number of incorrect solutions submitted. The list shall be sorted in descending order by the number of cryptograms solved.

**ANS:**  Data structure PlayersRatingList handles this requirement. This information is pulled from database and is sorted on the basis of &#39;TotalSolved&#39; attribute. (This format is taken from UML 2.2 Superstructure OMG Specification).

Req 13. The User Interface (UI) shall be intuitive and responsive.

**ANS:**  GUI is a general thing and should be left for the application designer&#39;s imagination and utility thought. It&#39;s not mentioned in the design.
