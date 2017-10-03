# Design Document

*This is the template for your design document. The parts in italics are concise explanations of what should go in the corresponding sections and should not appear in the final document.*

**Author**:  Team 47 

| Name | GT email ID |
| Isaac Silva | isilva6@gatech.edu |
| Mukul Pai | mpai8@gatech.edu |
| Saad Khan | skhan315@gatech.edu |

### Document Tracking

Following chart is used to log all the changes made to this document.

| Version | Date of edit/change | Who made the edit/change | Description of edit/change |
| :-----: | :-----------------: | :----------------------: | :------------------------: |
|    v1.0     |    10/03/2017                 |   skhan315 (Saad Khan)                       |           *first draft*                 |


## 1 Design Considerations

*The subsections below describe the issues that need to be addressed or resolved prior to or while completing the design, as well as issues that may influence the design process.*

### 1.1 Assumptions
<!-- *Describe any assumption, background, or dependencies of the software, its use, the operational environment, or significant project issues.* -->

This section enumerates all the assumptions that will impact the word scramble application design.

1. Version control will be handled using Georgia Tech’s GitHub. 

* Private team GitHub repository will be used to handle version control for the project.


2. The app will be a client-server design and will depend on ExternalWebService to handle communication between the client and central server. 

* Word Scramble game will be designed as a client/server application and will utilize the external web service (EWS) utiliity in order to communicate back and forth between the client (user/player) and the server.

3. The app will use as a gradle dependency Bootstrap for Android to develop the majority of the front-facing view. 

* DOUBLE CHECK

4. There will be basic authentication and unencrypted passwords.

* As per the UML design requirements, authentication is optional so the application will only require a unique username to login.


5. The app will use a fixed text-based, flat-file database that will be started on application startup.

* DOUBLE CHECK

6. Development deliverables will be delivered in a timely manner.

* It is intended that all the deliverables pertaining to development of the application will distributed in am appropriate and prompt way.

7. A waterfall approach will be used.

* DOUBLE CHECK

8. Testing will cover all functionality of the application.

* It is also intedend that the Test plan will account for all the various functionalities pertaining to the word scramble application.

9. Some pre-processing of cryptogram inputs may be necessary to ensure compatibility with database storage schemes and formatting.

* DOUBLE CHECK


10. Player Ratings will be handled as follows: Cryptograms will be counted as "started" once the solution phrase entry field is populated with any text and before it is submitted. Cryptograms with incorrect submissions will continue to count toward started cryptograms, but those with correct submissions will be counted only as "solved" (and no longer as "started"). Incorrect submissions will be increased for each incorrect submission, including multiple incorrect submissions for the same cryptogram.

* It is assumed that once a player has successfully logged in and wishes to initiate a particular game instance using the assocation class "PlayEvent", the game instance will have one of 4 stages for a player:

| Stage     | Description |
| :-------: | :---------: |
| RUNNING   | The time from which the solution letters are entered in the solution text box till the time submit button is clicked. In the case where the solution is incorrect, the game will remain in the running stage as neither a correct solution has been entered yet nor the player has saved their progress .|
| IN-PROGRESS | When a player leaves without submitting a solution, the game stays in this stage to keep record of any game that is in progress for that player.|
| SUBMITTED | In the case where the player clicks the submit button, the game moves to this state and will have to options to choose from, either move to the complete state (described below) or stay in the running state as the solution is incorrect up until that point.        |                
| COMPLETE  | When the solution letters submitted are for a correct solution, the state changes to complete, highlighting that a particular player has solved a scramble.    |                         
                 



11. It will not be necessary to create new administrators through the app user interface. An administrator account will be provided with credentials username: "admin" and password: Password" (without quotes).


* To start with, the application will be provided along with an initial user credential (username = player1) which will be considered as a demo user.  

12. Credentials (both username and password) may be case-sensitive and contain only alphanumeric characters.

* Username required for logging into or for creating a new player profile shall only contain alphabets and/or numerical characters. The username will also be case sensitive.

13. It is acceptable to be able to edit previously created cryptogram solution and encoded phrases, even if the requirements do not explicitly state this.


* The game will be able to accept infinte number of word scrambles before a player actually decides to save it to the system.

14. Only cryptograms in which every alphabetic character is shifted by the same number of positions in the alphabet (Caesar cipher or shift cipher) will be allowed when creating cryptograms. Additionally, cryptograms with same solution and encoded phrases (shift by 0 positions) will not be allowed.


* A valid word scramble will be the one where each alphabet or number is replaced at its position.

* The application will allow a player to save word scrambles with same solution but have different clues.

### 1.2 Constraints

*Describe any constraints on the system that have a significant impact on the design of the system.*

### 1.3 System Environment

*Describe the hardware and software that the system must operate in and interact with.*

## 2 Architectural Design

*The architecture provides the high-level design view of a system and provides a basis for more detailed design work. These subsections describe the top-level components of the system you are building and their relationships.*

### 2.1 Component Diagram

*This section should provide and describe a diagram that shows the various components and how they are connected. This diagram shows the logical/functional components of the system, where each component represents a cluster of related functionality. In the case of simple systems, where there is a single component, this diagram may be unnecessary; in these cases, simply state so and concisely state why.*

### 2.2 Deployment Diagram

*This section should describe how the different components will be deployed on actual hardware devices. Similar to the previous subsection, this diagram may be unnecessary for simple systems; in these cases, simply state so and concisely state why.*

## 3 Low-Level Design

*Describe the low-level design for each of the system components identified in the previous section. For each component, you should provide details in the following UML diagrams to show its internal structure.*

### 3.1 Class Diagram

*In the case of an OO design, the internal structure of a software component would typically be expressed as a UML class diagram that represents the static class structure for the component and their relationships.*

### 3.2 Other Diagrams

*<u>Optionally</u>, you can decide to describe some dynamic aspects of your system using one or more behavioral diagrams, such as sequence and state diagrams.*

## 4 User Interface Design
*For GUI-based systems, this section should provide the specific format/layout of the user interface of the system (e.g., in the form of graphical mockups).*


