# Project Plan

**Version**: 1.0<br>
**Author**: Team 47

## 1 Introduction

This project is an Android app that allows players to practice solving cryptograms and compare their scores with other players on the network. Administrators will be able to add new players and cryptograms in order to continuously expand the system.

## 2 Process Description

The following description lists activities categorized into the four phases of development as described by the Rational Unified Process: Inception, Elaboration, Construction, and Transition. Entrance and Exit Criteria are defined in terms of the main deliverables and documents that will be input and output to each activity.

### Inception Phase:
 
#### Develop a plan to execute the project
 
This activity will involve identifying the main tasks that will need to be achieved in order to successfully execute the program objectives. Developing this plan will involve linking the anticipated tasks to the main deliverables and scheduling them within the different phases outlined in the Rational Unified Process guidelines. This activity will also involve identifying what the primary roles within the team should be and matching team members with these roles according to skill and workload balance.
 
*Entrance Criteria*: Rational Unified Process guidelines<br>
*Exit Criteria*: Project Plan: Process Descriptions and Team Roles
<br><br>
 
#### Identify major users and actions
 
This activity is the first step in taking the project from an idea to an actual design, and involves interpreting the requirements to identify the main users or actors that will interact with the system or allow the system to function. These actors may be human or system actors. This activity also involves interpreting the requirements to identify the primary actions or tasks that will be accomplished by each of the actors, and the interaction between them. The results of this activity will be formalized as initial use cases and a use case diagram, but these outputs may evolve as the project progresses.
 
*Entrance Criteria*: General idea for system and Requirements<br>
*Exit Criteria*: Use Case Model: Use Cases and Use Case Diagram
<br><br>
 
#### Define system architecture
 
This activity will involve considering the major architectural components, assumptions, and constraints to the system. For example, whether or not the system should be a peer-to-peer or client-server design and what the operating environment will be. Some of these aspects of the design may be specified in the requirements while others may have to be inferred or tentatively selected. Graphical mockups can be constructed
 
*Entrance Criteria*: General idea for system, Requirements, and Use Case Model<br>
*Exit Criteria*: Design Document: Design Considerations, Component Diagram, Deployment Diagram, Class Diagram, User Interface Mockups
<br><br>

### Elaboration Phase:
 
#### Develop a plan to test the system
 
This activity will involve developing a general strategy for testing the system preliminarily defined by the Use Case Model and Design Document as it is actually developed. This plan will including the primary activities and techniques as well as test quality assessment and bug tracking. The tools that will be used to accomplish all these goals will also be identified. Finally, a preliminary set of test cases will be developed along with a template for tracking the progress of these test cases as the testing efforts progress along with development.
 
*Entrance Criteria*: Use Case Model and Design Document<br>
*Exit Criteria*: Test Plan: Testing Strategy and Test Cases
<br><br>
 
#### Identify extra or supplementary requirements
 
This activity will involve identifying any extra, non-functional requirements that are believed to be important enough to document but that may not fit into any of the other documentation. These requirements may include considerations such as reliability, maintainability, and security.
 
*Entrance Criteria*: Use Case Model, Design Document, and Test Plan<br>
*Exit Criteria*: Extra Requirements
<br><br>
 
#### Revise use cases and project plan
 
This activity will involve using what has been learned about the system during the preceding activities and deliverable development efforts to update the Use Case Model and Project Plan documents to better reflect the system and its requirements as they evolve.
 
*Entrance Criteria*: Preliminary Use Case Model and Preliminary Project Plan<br>
*Exit Criteria*: Updated Use Case Model and Updated Project Plan
<br><br>
 
### Construction Phase:
 
#### Code the initial version of app
 
This activity will involve taking the Use Case Model and Design Document and using them as a basis for beginning to code the required classes and method to accomplish the software goal of the project. The class diagram in particular will be used to inform the construction of classes and the use cases will inform the behavior of the app. This activity will involve coordination of both “back-end” functionality and “front-end” user interface development tasks. The result should be a functional application that realizes all the use cases, but may still contain some features that require further work or testing.
 
*Entrance Criteria*: Use Case Model, Design Document, Extra Requirements<br>
*Exit Criteria*: Initial App Release (all use cases realized and traceable)
<br><br>
 
#### Begin running test cases
 
This activity will involve beginning to validate that the app as developed is meeting the requirements and executing the features as desired. 
 
*Entrance Criteria*: Initial App (at least partially done), Test Plan<br>
*Exit Criteria*: Updated Test Plan with updates to Test Case results
<br><br>
 
#### Compile a user manual
 
This activity will involve taking the previously defined design documents as well as experience with the initial release of the app in order to produce a document meant to be read by the end-user in order to explain to them how the app works and what they can do with it.
 
*Entrance Criteria*: Use Case Model, Design Document, Extra Requirements, Initial App Release<br>
*Exit Criteria*: User Manual
<br><br>
 
#### Revise earlier documents
 
This activity will involve updating any of the previously generated documents such as the Project Plan, Use Case Model, Design Document, Extra Requirements, and Test Plan with new or revised elements based on changes as the actual application is developed. Because of the iterative nature of development, the team’s understanding or interpretation of how all the requirements should be met may evolve over time and these changes should be reflected in the final documentation.
 
*Entrance Criteria*: All previous documentation, Initial App (at least partially done)<br>
*Exit Criteria*: Updated versions to any document required in order to reflect the actual design
<br><br>
 
### Transition Phase:
 
#### Refine application
 
This activity will involve finalizing all app features as well as addressing any issues that arise as the result of thorough testing. These changes could include both improvements to user experience elements and the fixing of bugs in the functionality.
 
*Entrance Criteria*: Initial App Release<br>
*Exit Criteria*: Final App Release
<br><br>
 
#### Begin running test cases
 
This activity will involve continuing to validate the functionality of the app to ensure that it is properly fulfilling every aspect of the finalized use cases and design requirements. By the end of this activity the app should be finalized and all test cases should be passing.
 
*Entrance Criteria*: Initial App/Final App, Test Plan<br>
*Exit Criteria*: Finalized Test Plan with complete Test Case results
<br><br>

 
#### Revise earlier documents
 
This activity will involve updating any of the previously generated documents and will be very similar to the activity with the same name in the previous construction phase. In reality, it is a continuous process to ensure that the documentation reflects the actual app in its final state.
 
*Entrance Criteria*: All previous documentation, Final App<br>
*Exit Criteria*: Updated versions to any document required in order to reflect the actual design
<br>

## 3 Team

### Team Members:
 
Team members include Michael Amadasun, Alexander Molnar, Muzammil Mueen, and David Nelson.
 
### Roles:
 
**Application Software Developer**: This role will involve taking primary responsibility for developing the underlying data structures and functionality to accomplish the design requirements and use cases. The Functionality Developer also coordinates the “back-end” tasks and any required communication with the ExternalWebService and local database.
 
**User Interface Software Developer**: This role involves taking primary responsibility for developing the “front-end” elements of the application such as the user interface and user experience. The User Interface Developer creates the graphical mockups and works with the Functionality Developer to ensure that the user interaction elements are coordinated with the classes and methods underneath.
 
**Application Designer/Documentation Lead**: This role involves taking primary responsibility for the overall architecture and how the design accomplishes the requirements. The Application Designer/Documenter takes primary responsibility for taking input from other team members and creating and maintaining the documentation and deliverables that reflect these design choices as the project progresses through all the phases.
 
**Application Tester**: This role involves taking primary responsibility for all testing that will be performed on the application, including black-box testing and white-box testing. The Application Tester also maintains and updates the Test Cases as required, including updating whether or not they are passing in the latest version of the app and informing the other developers when there appears to be a design problem or a bug.

### Role Assignments:

| Team Member Name   | Role                                    |
| :----------------: | :-------------------------------------: |
| Michael Amadasun   | User Interface Software Developer       |
| Alexander Molnar   | Application Tester                      |
| Muzammil Mueen     | Application Software Developer          |
| David Nelson       | Application Designer/Documentation Lead |
