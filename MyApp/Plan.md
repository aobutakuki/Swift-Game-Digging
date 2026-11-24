This is a SWIFT Mining Game as a first project.

This project will present a huge challenge as this will be one of my first real projects outside of C++, and my first mobile experience.
To make sure everything goes to plan I will start by planning what we want the general concept to be, classes, structs and will attempt to focus on make everything modular and not dependent on one another.
We must also ensure the game performs well and does not consume any memory that is not needed.

**Concept**
This will be a mining game, the user will:

1. Mine blocks and sell then for in-game currency
2. Upgrade their gear using in-game currency
3. Mine further down, each level will present new blocks
4. Be able to upgrade, tools and gear to shape the world as the user likes
5. Progress must be saved

This means, the user will start with basic tools, slow, weak and progress themselves into a more robust enviroment that will present the user with bigger challenges.


---
**How should we store each component?**

Game Tiles -
Game tiles need a data type that support
1. Tile Hardness - basically the tile HP
2. Tile Type - like a enum class in c++
3. Tile Texture - dirt, stone, diamond
4. Tile Base Price - dirt $1, diamond $1000, etc


The Player - 
The player must be able to move, and hold tools, as well as perform different actions
1. Mine
2. Health
3. Stamina
4. Hold Tools
5. Place Items


The User - 
This data structure must hold configuration files and settings
1. In-game progress
2. Settings (audio, movement)
3. Highest Score
4. In-Game Money


The Game -
The game must alter how we behave in the world
1. Menu Screen
2. Settings
3. UI Interface for displaying data (maybe general function)
4. Game Loop
5. Speed
6. Physics


Movement Engine - 
This allow us to pass a command into an object, enemy or the player, such as walk or jump.
1. Player movement (drag the finger anywhere in the screen)
2. Dig - click and hold anywhere in the screen
3. Interact - click anywhere in the screen


Audio - 
Each component needs an audio action, we will structure this as a service:
Struct -> Sends Message -> Audio Component -> Replies with audio
This way we do not keep the audio component coupled with anything, just as message service.

Our game must follow DRY Principles, avoid code duplication, and be fun to play.



