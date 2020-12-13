## Architecture 

------

##### Architecture Design Diagram

<img src=".\ArchitectDesignFin.png" style="zoom:72%;" />

##### Architecture Description

The above diagram depicts the use of a mixed Architecture. The architectural styles that I used in this diagram are Pipe-and-Filter and Layering. Reasons for the Pipe-and-Filter is that the implementation of the ongoing design is not dependent on the previous filters that were implemented before. This means it is easy to add and remove filters at will. This is the case when the format of the data is fixed. There is no parsing of tokens, as is the case with compilers, and the data is not needed to be written to another language. Our project is coded entirely in Python, therefore the data represents a fixed format. The Layer style is good for representing dependencies. In a layered architecture, the layer below provides services to the layer above it and the above layer acts as a client to the layer below it. The layer design is not a 'pure' layer system, meaning that one layer is not restricted to accessing the units at the layer or services provided by the layer immediately below it. There are instances where a layer is bridged to another layer. I will go into further detail about those instances below. 

 The Player first starts the game by selecting 'play game' at the main menu. The game will initiate the movement of the enemies and the player will begin movement of the player sprite. The movement of the enemies is automated, whereas player movement is accomplished with the use of a user-defined method that belongs to the the Player class. The units available to both enemy and player movement are variables that hold the position of the player and enemy at the screen. The amount of change in x-axis depends on how many times the player pressed the right or left arrow keys. As you remember, the movement is accomplished by the update procedure (method). 

Both player and enemy have a primary basic attack. The bridge of 'Drop Powerup' to 'Obtain invincibility Powerup' happens when the player comes into contact with the invincibility powerup. The specificity of the powerup type initiates the invincibility animation and powerUpPlayer procedure, with the invincibility type as the argument, should be carried out. 

The piping of the attack shot on the player to enemy or the enemy to player will pass through a filter that will then initiate the proper procedure based on the event that commenced. The filter that is labeled 'Comes into Contact' will call a procedure based on what event occurred. The contact of the enemy with the player will further call the 'check_health_remains' procedure. The top 'Comes into Contact' filter has the same context. The difference is that the player attack will come into contact with the enemy or powerup blimp. The appropriate procedure calls will happen based on which of the two events occurred.

The completion of the removal of all enemies from the screen will initiate the procedure of initiating the load of the next level. The level will be have the player defend himself against a new wave of enemies. The levels will continue to load until all the levels are completed. At this point, the boss battle will commence. Update on the Boss battle architecture will be revealed soon. 