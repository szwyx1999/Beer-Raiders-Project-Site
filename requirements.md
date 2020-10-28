## Initial Requirements

------

##### **Context of Product**

Our team's product will be used in a home or school/workplace environment. The product is a playable game that will be hosted on a Personal Computer. I say that the environment includes the school or workplace because many users will play our game on their laptop. The laptop has the ability to be carried along to different environments. There are many environments that I have not listed that could be listed, but for simplification I have limited the environments to home or workplace. 

##### **Domain Model with Description**

<img src="C:\Users\cdavila\Documents\CS_371\Beer-Raiders-Project-Site\UMLclass.png" alt="UMLclass" style="zoom:65%;" />

The above UML Class diagram depicts the game system mechanics. The Player has a relationship with Enemies in that the player attacks the enemies. The multiplicity on the enemies end indicates that there will be 1 or more enemies attacking one Player. At all times, there will be only one player attacking one or more enemies. The Scores Points association class indicates that the moment a player attacks and hits an enemy, the moment is recorded as points scored. The Lose Health association class indicates the player is penalized with a loss of health the moment an enemy's attack hits the player. Because the player is able to accumulate more one instance of points, the player is composed of a score. The Score composition class is indicative of the upkeep of an aggregate score. During the player's game, the score will accumulate to a specific amount and grant the player one extra health. The PointsNeedToExHealth attribute representative of a constant and the AggregateScore attribute is checked against the PointsNeedToExHealth attribute to find if the player is successful at reaching the required amount of points specified in the PointsNeedToExHealth attribute. 

The PowerUp Dropped association class is dependent on the attacks association between the Player and Enemies. This relationship indicates that there will be an item dropped during a specific time interval, granted the player has hit the blimp carrying the powerup with his or her attack. The next appearance of a blimp is reliant on the time the previous blimp appeared in the game. The PowerUp composition class indicates that the player will have obtained multiple powerups throughout his or her gameplay. The powerup will have a 1 or many  to 1 relationship with the Player.  The player will be granted the powerup on top of the powerup that the player currently has. Each powerup remains in use for a specific amount of time or until the player is hit with an attack. The Blimp class will generate the Blimps carrying the powerups onto the screen at specific time intervals to allow for the player to obtain different powerups.    

Both the player and Boss have instances of health progression and digression. The class methods and members can be implemented in the Player class, but the separation shows that the class Player and the subclass Mothership both share instances of health. Therefore, the Player and Mothership will have to have an Aggregate Health member and CheckIfHealthRemains() method. 

The Mothership and UFO enemy types are both subclasses that inherit class members and methods from the Enemies superclass. This is indicated by the sub-type relation contained between them and the Enemies class. Moreover, Score and PowerUp classes can be implemented as sub-classes of Player, but the preferred implementation is to have it be a composite of the Player class. 

##### **User Characteristics and Expectations**

The users of the game are semi-skilled game enthusiasts to new and un-skilled gamers. The game's controls are easy to understand, and the game's user interface does not have components that need explaining. The components are self explanatory because there are labels for score and Health. Powerups that are obtained by the player would be described at the beginning of the game through the use of an instruction screen. Instructions displayed will be player movement controls and descriptions of each powerup and their effects on the user.

I understand that the user will want some functionality in terms of different levels and increasing difficulty as levels progress. This expectation was addressed in the user stories document. It is of importance to ensure a player is presented with a steady playthrough without having too great of a challenge as well. That is why having an increase of powerups appear during the higher difficulty levels is important. The process of finding out the playability of the game will be further inspected by conducting interviews with the players who play the game.  