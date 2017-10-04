# Design Document

<!-- *This is the template for your design document. The parts in italics are concise explanations of what should go in the corresponding sections and should not appear in the final document.* -->

**Author**:  Team 47 

| Name | GT email ID |
| :-----: | :-----------------: |
| Isaac Silva | ```isilva6@gatech.edu``` |
| Mukul Pai | ```mpai8@gatech.edu``` |
| Saad Khan | ```skhan315@gatech.edu``` |

**Document Tracking**

Following chart is used to log all the changes made to this document.

| Version | Date of edit/change | Who made the edit/change | Description of edit/change |
| :-----: | :-----------------: | :----------------------: | :------------------------: |
|    v1.0     |    10/03/2017                 |   Team 47                       |           *first draft*                 |


## 1 Design Considerations

<!-- *The subsections below describe the issues that need to be addressed or resolved prior to or while completing the design, as well as issues that may influence the design process.* -->

This section contains all of the assumptions, system dependencies and constraints that were considered during the design of each subsystem and component of the word scramble application.

### 1.1 Assumptions
<!-- *Describe any assumption, background, or dependencies of the software, its use, the operational environment, or significant project issues.* -->

TAn android mobile pplication is dependent on the Web Application because the mobile application cannot work without the data from the web application and vice versa. 

This section enumerates all the assumptions that will impact the word scramble application design.

| **No.** | **Description** |
| :---: | :--- |
|1. | The Word Scramble android game will be designed as a client/server application and will utilize the external web service (EWS) utiliity in order to communicate back and forth between the client (user/player) and the server. |
|2. | As per the UML design requirements, authentication is optional so the application will only require a unique username for a particular player to login.|
|3. | The intention of the application development team is that all the deliverables pertaining to development of the application will be distributed in a appropriate and prompt way.|
|4. | It is also intedend that the test plan will account for all the various functionalities pertaining to the word scramble application.|
|5. | Private team GitHub repository assigned by Georgia Tech will be used to handle version control for the group project.|
|6. | It is assumed that once a player has successfully logged in and wishes to initiate a particular game instance using the assocation class "PlayEvent", the game instance will have one of 4 stages for a player: RUNNING :- The time from which the solution letters are entered in the solution text box till the time submit button is clicked. In the case where the solution is incorrect, the game will remain in the running stage as neither a correct solution has been entered yet nor the player has saved their progress.I N-PROGRESS :- When a player leaves without submitting a solution, the game stays in this stage to keep record of any game that is in progress for that player. SUBMITTED :- In the case where the player clicks the submit button, the game moves to this state and will have to options to choose from, either move to the complete state (described below) or stay in the running state as the solution is incorrect up until that point. COMPLETE :- When the solution letters submitted are for a correct solution, the state changes to complete, highlighting that a particular player has solved a scramble.    |  
|7. | To start with, the application will be provided along with an initial user credential (username = player1) which will be considered as a demo user. |
|8. | Username required for logging into or for creating a new player profile shall only contain alphabets and/or numerical characters. The username will also be case sensitive.|
|9. |The game will be able to accept infinte number of word scrambles before a player actually decides to save it to the system.|
|10. |A valid word scramble will be the one where each alphabet must be replaced at its position. None of the letters in the phrase should be left unscrambled.|
|11. |The application will allow a player to save word scrambles with same solution but have different clues.|
----------------------------------------------------------------------------------------------------------------------

12. The development process for the application will follow the waterfall model only moving into the next phase once the previous one is finalized.

13. ARE WE GOING TO PRE_PROCESS TEH WORD SCRAMBLE AND CLUE IN ANY WAY FOR EASE OF STORAGE OR FOR EASE OF FORMATTING

14. gradle dependency Bootstrap for Android any ASSUMPTION

15. The applicaiton will use a flat text based approach to take user input for the original phrase, scrambled phrase, solution phrase and the clue.          



### 1.2 Constraints

<!-- *Describe any constraints on the system that have a significant impact on the design of the system.* -->

1. Word Scramble application will be programmed using Android Studio version 2.2.
2. If programming outside of Android Studio is neccessary, IntelliJ Idea IDE with Java version 1.8 will be used where required.
3. Team will try to deliver the project within the allotted time period.
4. Huge amounts of data shall not be stored on the application (android phone)
5. Internet access shold be available for the application to execute properly.
---------------------------------------------------------------------------------------------
6. 
7. 

### 1.3 System Environment

<!-- *Describe the hardware and software that the system must operate in and interact with.* -->

1. Word Scramble application will be created with a minimum targeted sdk version of 19, i.e application will be operational under API level 19.
2. Fully working application should be able to run at default screen resolutions on standard android phones.
3. At software testing level, application will be tested on Nexus 5 API 24 (Android 7.0, API 24) Android Emulator.
----------------------------------------------------------------------------------------------------------------

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


