# Tourney Manager Group Project - Deliverable 1

This assignment is a continuation of the Tourney Manager application. Group 2 has    
collaborated together, analysing their individual designs, with the attempt to   
create an agreed upon 'final design'. 

## Background

Leeroy is happy that you have given him a design for his Tourney Manager application in   
Assignment 5. Perhaps you should have expected it from anyone running a tournament ring in a   
college dormitory, but he has also requested designs from all of his other friends, and would   
now like to see what a team of programmers can accomplish to help him manage his egaming   
tournaments. He has therefore requested that a team of you complete a group design, by   
following the instructions he has provided below. Because Leeroy is also studying computer   
science and is familiar with UML, he wants the design to be represented using a UML class   
diagram. Luckily, the members of your team have some recent practice with this, so the team   
should be able to hit the ground running and produce a good design quickly.

## Individual Designs

### Design 1

![Design 1 - UML](https://www.dropbox.com/s/v7ch5oyitni33xg/design1.png?raw=1)

**Pros:**
* There is a TournamentUser class, that has Player and manager has child classes.
* Matches aggregates Tournaments
* Most classes are the same as the other designs.
* Cardinality is marked appropriately 
* Methods are provided with a data type
* Utilities included

**Cons:**

* While the PastTournament class could serve as a subclass, Java doesn't really support object    
transformations. The Tournament class should suffice.
* While the CurrentTournament class could serve as a subclass, Java doesn't really support object    
transformations. The Tournament class should suffice.
* Should there be more attributes listed in the Tournament match to identify a unique match.
* Little cardinality is shown.

---------------------------------------

### Design 2

![Design 2 - UML](https://www.dropbox.com/s/h5bc55lnnfbza4g/design2.png?raw=1)

**Pros:**
* Most classes are the same as the other designs.
* Relationship texts show clear actions impacted on other classes
* Classes are given unique IDs to distinguish them in the database 

**Cons:**
* Relationship between TournamentPlayer and Tournament should be written as 8, 16 (discrete values)
* Manager and Player can be a child of a User class.
* A tournament is made of many matches, use the diamond for aggregation.
* Should the deck be a Class (a deck can be a tangible item, thus an object at some point in time.)
* Cardinality between relations are incorrect
* Does not show the mode or database as utility classes 
* Data types are not provided with the attributes and methods

---------------------------------------

### Design 3

![Design 3 - UML](https://www.dropbox.com/s/zewlo061newxpa1/design3.png?raw=1)

**Pros:**
* Most classes are the same as the other designs.
* Relation cardinality is clearly defined
* Method labels are clear to understand

**Cons:**
* Methods are not on the classes which should be affected by the action. Many classes are affected by this:
* ShowPlayerTotal() should be in the Player class.
* Manager class should not contain methods.
* Should mode be its own class? 
* Should attributes be provided for each player in match? 

## Team Design
### Final Team Design

![Team - UML](https://www.dropbox.com/s/k5rwcz5ltuswyra/team.png?raw=1)

### Commanalities and Differences
The primary commonalities that were found in the individual designs were the classes themselves. The class    
definitions were interpreted generally in a similar fashion across the individual designs

Some of the primary differences, however, were in how the individual designs interpreted which requirements    
impacted the design of the UML diagram. In one design, the Mode was shown as an individual class. In another, Mode    
was interpreted as a Utility class. And in the third design it was not represented at all. This was also similarly the case    
for the database and the Deck Choice of the player. 

In the final design we resolved the differences between the individual designs by including database as a utility class,    
Mode and Deck also as classes, and finally removing the remaining two uncommon classes that were not seen across all    
individual designs. We felt that including the database as a utility was appropriate given the video demonstration in the    
Udacity lesson showing utility classes being used in a similar manner. We also felt that mode should be considered a class,    
as it will instantiate either the tournament manager or tournament player workflow upon startup and selection. Deck was also    
considered to be a class, as it is a tangible entity in the real world, and therefore impacts the design of the UML diagram. 

## Summary
In conclusion, we found that our individual designs were generally already well aligned. The individual designs only required    
minor clarification to gain consensus on what the team design should look like. We believe a key lesson learned is the    
open-ended nature of analysing requirements. In particular, how one requirement can not only be interpreted in multiple ways, but also be satisfied sometimes in as many ways as it is interpreted as long as the expected result is provided from the requirement.  
