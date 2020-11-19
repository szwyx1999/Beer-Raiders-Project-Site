## Design Document

------

##### Architecture and Description

<img src=".\ArchitectDesignFin.png" alt="ArchitectDesignFin" style="zoom:74%;" />

The above architecture is the final product. I have reviewed the previous architecture and found this architecture to best describe our game's mechanics. The mechanics are initiated at the procedure calls. The player first starts the game by selecting 'game start' from the main menu screen. The commencement of the game starts the enemy and player movement procedures. The player is in control of the player movement, whereas the enemy movement is automated. Player attack is also controlled by the player, and the enemy will have automated shooting mechanics. Next procedure from movement is the enemy or player attack. These attacks will eventually come into contact with either the enemy or player. Attacks occur simultaneously at times, therefore the layers of procedures are inline with one another. 

The player has different objects that he or she can attack. The main objects are the enemies, and the secondary are the blimps that carry powerups. When a blimp is generated the player will attempt to destroy the blimp to force the powerup to drop to the player's ground level. If the player comes into contact with the powerup, the powerup will alter the player's abilities accordingly. One powerup will cause the player to obtain a rapid fire ability. The other is a temporary immunity to enemy attacks. Proper procedure calls are commenced with the appropriate power up type as an argument to alter the player's abilities. 

Once all the enemies are exploded, the next level is brought to the forefront and the player will continue to attempt to explode all the enemies on the screen. Each level will gradually increase in difficulty during the player's attempt to reach the boss. The player will have a health meter in the form of beer bottles and a single beer bottle will be removed after each successful enemy attack. The health of the enemy will be checked to see if health remains. The game is over when no health remains. 

As stated before, the levels are served to the player after every enemy on screen has been exploded. The new level filtering directs a procedure calls on player and enemy movement. This is process loops until the player has defeated all levels. Once all levels are defeated, the player is brought to the boss level. This triggers the continuation of player and enemy movement procedures, with the difference being there is one big enemy instead of multiple small ones. Continuation of the player's objective to destroy all enemies on screen is reassigned and commenced. From here the player will attack the boss or powerup blimps. The player will continue to have access to rapid fire or invincibility powerups and the player's attacks will come into contact with either the boss or powerup blimps. 

The boss will take a certain amount of hits from the player's attacks to be destroyed. Therefore, the attacks will continue until the boss has no health remaining. At the point of no health, the boss will explode and the game will end. The game will end with text indicating the successful completion of the main objective. All units that are displayed are attributes that were assigned to classes in the class UML diagram. The procedures are class methods. The finished game will contain the methods and attributes contained within their appropriate classes. 

##### Initial Requirements

Refer to the requirements document to see the updated UML class diagram with description. 