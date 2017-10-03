# Design Document

*This is the template for your design document. The parts in italics are concise explanations of what should go in the corresponding sections and should not appear in the final document.*

**Author**:  Team 47 *(Isaac Silva - Mukul Pai - Saad Khan)*

### Document Tracking

Following chart is used to log all the changes made to this document.

| Version | Date of edit/change | Who made the edit/change | Description of edit/change |
| :-----: | :-----------------: | :----------------------: | :------------------------: |
|         |                     |                          |                            |
|         |                     |                          |                            |
|         |                     |                          |                            |
|         |                     |                          |                            |

## 1 Design Considerations

*The subsections below describe the issues that need to be addressed or resolved prior to or while completing the design, as well as issues that may influence the design process.*

### 1.1 Assumptions

[comment]: <> (*Describe any assumption, background, or dependencies of the software, its use, the operational environment, or significant project issues.*)

This section enumerates all the assumptions that will impact the word scramble application design.

1. Version control will be handled using Georgia Tech’s GitHub.
2. The app will be a client-server design and will depend on ExternalWebService to handle communication between the client and central server. 
3. The app will use as a gradle dependency Bootstrap for Android to develop the majority of the front-facing view. 
4. There will be basic authentication and unencrypted passwords.
5. The app will use a fixed text-based, flat-file database that will be started on application startup.
6. Development deliverables will be delivered in a timely manner.
7. A waterfall approach will be used.
8. Testing will cover all functionality of the application.
9. Some pre-processing of cryptogram inputs may be necessary to ensure compatibility with database storage schemes and formatting.
10. Player Ratings will be handled as follows: Cryptograms will be counted as "started" once the solution phrase entry field is populated with any text and before it is submitted. Cryptograms with incorrect submissions will continue to count toward started cryptograms, but those with correct submissions will be counted only as "solved" (and no longer as "started"). Incorrect submissions will be increased for each incorrect submission, including multiple incorrect submissions for the same cryptogram.
11. It will not be necessary to create new administrators through the app user interface. An administrator account will be provided with credentials username: "admin" and password: Password" (without quotes).
12. Credentials (both username and password) may be case-sensitive and contain only alphanumeric characters.
13. It is acceptable to be able to edit previously created cryptogram solution and encoded phrases, even if the requirements do not explicitly state this.
14. Only cryptograms in which every alphabetic character is shifted by the same number of positions in the alphabet (Caesar cipher or shift cipher) will be allowed when creating cryptograms. Additionally, cryptograms with same solution and encoded phrases (shift by 0 positions) will not be allowed.

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


