# CS6300 SDP Fall 2017 - Group Project
by Isaac Silva (```isilva6@gatech.edu```), Mukul Pai (```mpai8@gatech.edu```), Saad Khan (```skhan315@gatech.edu```)

## Word Scramble Game

## Individual Designs

### Design 1

![Isaac Silva's Design](designs/design_Isaac_Silva.png)

- Excellent portrayal of the overall system to be implemented - very easy to visualize the overall design of the system.
- Accurate mapping of requirements. Incorporated all the functional requirements that the system needs, to behave as expected.
- Class components described are consistent i.e all components  accurately displays class specific attributes and functions.
- Interaction between the components are showcased explicitly.


Overall Good job done in incorporating all the requirements while keeping it simple and clean. (in contrast to my design where I have added scrupulous details which now I think is not required at this phase of design)

Note: Post our monday night’s discussion and me going over the requirement specs again, it makes sense to have a simple abstract design for our Phase 1 design and can take Isaac’s design as base and then add on to it. Like for instance showcasing Statistics class and if needed the persistence layer  as per Saad’s insight. 

The UML design shown above was created by Isaac Silva. One of the main highlight for this design is that it is very clean and very well organized. The design avoids extra cluttering by including most of the design requirements within four modules. Design also uses a combination of getter and setter methods encompassing good programming practice. Concise explanation of each connection is another useful feature of the design.

As an entry point to the application, the designer uses a 'User' class by including most of the essential design requirements such as creating a new player, viewing player statistics, maintaining game progress, solved game list, etc. Similarly, the 'Game' class, quite aptly, handles everything pertaining to the word scramble game as well as the statistics. The external web service utility also appropriately addresses the design requirements.

On the other hand, the UML did not include any underlying database, which seems to be necessary for the application. Although, the design in less cluttered with minimal modules, however, to make the design easier to implement a few additional modules addressing specific tasks such as dedicated module to statistics, creating a new player, etc would have been more appropriate from implementation point of view.




### Design 2

![Mukul Pai's Design](designs/design_Mukul_Pai.png)


-	having a statistics class to encapsulate the logic of how to get the statistics is a good idea.
-	The response of each method call could include  the data types in more details to facilitate comprehension of what the method is actually returning. For example, the Statistics object that gets returned by a few method calls does not contain any properties in the UML design, only methods, which makes it hard to understand what that type is representing
-	Couldn’t understand what Loggedin is a particular type and not just a property of a User Session Type for example. 
-	Not sure if player and user should have a one to many relationship. That was not clear in the requirements doc.
-	The state of scramble (in-progress, completed) as different class types is confusing. 
-	The overall design seems to have many types, which makes it a bit hard to understand.
-	The methods defined in the utility class are slightly different from what the requirements doc stipulated, more specifically the statistics method. Maybe they could have been written in a more declarative way.


The design presented above was created by Mukul Pai. This design expresses cardinality quite appropriately between the 'User' and the 'Player' and then between the 'Player' and the 'Scramble' classes. Another highlight of the design is that object oriented approach is clearly defined between the 'Scramble' class and associated classes 'NewScramble', 'ProgressScramble', etc & then between the 'Statistics' class and 'PlayerStatistics' and 'ScrambleStatistics' classes.

Similar to the rest of the team members, the design uses a 'User' class as an entry point to the application handling all the information that is required to create a new player. Along with that, the Scramble class and its associated classes clearly separated and address all what was required as part of the design requirements. This can be very positive in the sense that it provides better understanding of what the application implementation approach should be like.

On the contrary, above mentioned aspects of the design are sort of positive as well as negative. That is having a more detailed UML design can be very apt in some cases, however, a more simpler design could have been more appropriate as some of the additional classes could have been engulfed into the parent classes. Another thing not present in the diagram was an underlying database to handle player, scramble and statistical information.


### Design 3

![Saad Khan's Design](designs/design_Saad_Khan.png)


-	There are 3 classes to describe a user. It seems a bit too much. For example, New Player should not be a class but an instance of a class.
-	View scramble statistics method should be part of the scramble domain not the user domain. 
-	createWordScramble should be an instance of the WordScramble class. It doesn’t not have to be represented as a type.
-	Database representation should not be part of the UML data model.
-	The external utility class should be directly used by the instances of the other types (i.e. User , Scramble) not by the database.
-	The solveWordScramble class should not be described as a class but as a method of the WordScramble class
-	There are too many class types in general. The design can be simplified. 

- From a point of view of an user application the design  excellently covers all the components to be involved in the application with accurate interactions and flow. 
- Good design principles has been followed to showcase Component attributes and the their functionalities .
- After review on my own design I think we can exclude createWordScramble and solveWordScramble from the design and keep those at implementation level.  
- We can finalize on whether to include the persistence layer or not in our next meeting
- EWS seems to me a centralized utility accessed by all other components in the system. Need a tweak to showcase this in the design.

Overall nice job. Also I see similarity in my and Saad’s design approach like including statistics class, and having multiple instances of Scramble. Seems we can exclude some of these and keep the design abstract at this phase. 



## Team Design
![Team Design](designs/design_team.png)


## Summary

Main objective of coming together as a team for the final design was quite useful as a general review excel sheet was shared amongst the members before the team met collectively to work on the final design. This way, each team member was able to perform first draft of the review for other team member's design. This left each team member and the team collectively in a better position to address the do's and don’ts for the final design and by the time the team got together to discuss the final design each member had a clear idea of what was to go into the design.

The whole experience of team work highlighted both theoretical and industrial practices of software development process. This approach and the feedback from within the team also helped each team member to review the capabilities of their own individual design. Building the final design was an iterative process with team observing and mitigating possible design shortcomings along the way.

The team also took the approach of coming up with a completely new design by re-visiting the requirements for assignment 5. Although, the final design was a mixture, more mature version of each team members design, re-visiting the requirements helped the team address the task at hand in a much better way.

Finally, when compiling the team design, members put extra effort to make it a nice amalgamation of each individual's design and precisely portraying what was required of it without making it too intricate.
