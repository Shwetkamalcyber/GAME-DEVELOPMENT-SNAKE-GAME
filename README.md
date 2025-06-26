# GAME-DEVELOPMENT-SNAKE-GAME
COMPANY: CODTECH IT SOUTION 

NAME: SHWET KAMAL

INTERN ID: CT04DF161

DOMAIN: C++

DURATION: 4 WEEKS

MENTOR: NEELA SONTASH

#DESCRIPTION:

The provided C++ code implements a classic Snake Game using the SFML (Simple and Fast Multimedia Library) framework. It features real-time gameplay, dynamic graphics, sound effects, and music, making it an engaging project that integrates core concepts of game development, object-oriented programming, event handling, and multimedia processing.

Game Overview
In this game, the player controls a snake that moves across a grid-based window. The snake grows longer each time it eats food and the goal is to achieve the highest score possible without colliding with the walls or itself. The difficulty increases gradually as the snake speeds up after every few points.

Window and Graphics Setup
The game window is created using SFML’s RenderWindow class with a fixed size of 800x600 pixels. The playing field is divided into square cells of size 20x20 pixels, allowing the snake to move in discrete steps along a virtual grid. Snake segments are rendered using green rectangles (RectangleShape), and the food is represented by a red circle (CircleShape).

Core Game Mechanics
At its core, the game loop consists of three main operations:

Event Handling (processEvents):
This function listens for user inputs. Arrow keys are used to control the snake’s direction, and pressing ‘R’ resets the game after a collision. The direction cannot be reversed immediately to avoid self-collision due to fast key presses.

Game Update (update):
If the game is not over and the elapsed time exceeds the current speed threshold, the game state is updated. The move() function shifts each segment of the snake to the position of the previous one, and the head moves one cell in the current direction.

Collision Detection (checkCollision):
The game checks for three types of collisions:

Wall collision: If the head moves beyond the window bounds.

Self collision: If the head overlaps any part of the body.

Food collision: If the head reaches the food, a new segment is added, score is increased, a sound plays, and a new food item is spawned randomly on the grid.

Dynamic Difficulty and Scoring
The scoring system is simple but effective. Every time the snake eats food, the score increments by one and the game becomes slightly faster. This is controlled by dynamically adjusting the speed variable based on the score:


speed = std::max(0.05f, 0.1f - score * 0.005f);
This ensures that the game remains challenging as the player progresses.

User Interface and Audio
A basic UI is implemented using SFML’s Text class to display the current score in the top-left corner. The game also includes:

A game-over message shown in red at the center of the screen.

Background music played in a loop (background.ogg).

Sound effects for eating food (eat.wav) and for game over (gameover.wav).

All fonts and audio files are loaded from an "assets" directory, and SFML’s resource management makes this seamless.

Game Reset Mechanism
The reset() function reinitializes all variables, clears the snake body, and restarts the game clock. It ensures a fresh start without needing to close and reopen the game window.

Object-Oriented Design
The entire game logic is encapsulated in the SnakeGame class, promoting modularity and clarity. This design makes the code scalable for adding features like levels, menus, or multiple difficulty settings.

Conclusion
This SFML-based Snake Game is a well-structured and fun-to-play application that demonstrates real-time graphics, input handling, and basic AI-like behavior. It provides a strong foundation for beginners learning game development in C++, while also showcasing how simple elements can come together to create a full-fledged interactive application.

#OUTPUT:

