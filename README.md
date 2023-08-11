# eggEscape Game - Technical README.md

---

## Introduction

**eggEscape** is a canvas-based web game developed using HTML5 and JavaScript. It leverages the Canvas API for rendering and game loop management. The game's architecture is based on a modular class structure that promotes separation of concerns.

---

## Game Architecture

### Classes

1. **Game Class**: 
    - Serves as the central game controller.
    - Manages game state, updates, and rendering.
    - Houses main game loop mechanics.

2. **Player Class**: 
    - Represents the main user-controlled character.
    - Attributes include position (`collisionX`, `collisionY`), speed (`speedX`, `speedY`), and sprite properties.
    - Collision detection mechanics are embedded using the `collisionRadius` attribute.

3. **Egg Class**: 
    - Represents in-game collectibles.
    - Attributes primarily revolve around positioning and state on the game canvas.

4. **Enemy Class**: 
    - Represents the game antagonists.
    - Similar attributes to `Egg`, but with added behaviors and potential interactions with the `Player`.

### Core Mechanics

- **Collision Detection**: Utilizes the `collisionRadius` attribute across entities to detect overlaps and interactions.
- **Sprite Animation**: Dynamic sprite selection based on movement direction, leveraging the `frameX` and `frameY` attributes.
- **Timed Mechanics**: The game incorporates a hatch timer (`hatchTimer`), potentially influencing game strategy and outcomes.

---

## Technical Considerations

- **Rendering**: The game employs double buffering for smoother animations, leveraging the canvas context's `fillStyle`, `strokeStyle`, and related methods.
- **Event Listeners**: Player movement is dictated by mouse events, which adjust the `speedX` and `speedY` attributes.
- **Performance**: For optimal performance, especially during collision checks, certain optimizations like quad-trees or spatial partitioning may be considered in future updates.

---

## Development & Setup

1. Clone the repository.
2. Ensure you have a web server (e.g., Apache, Nginx) or use tools like `live-server` for local development.
3. Load the main HTML file in a web browser to start the game.

---

## Contribution Guidelines

- **Code Structure**: Adhere to the modular class-based structure.
- **Performance**: Any updates should be tested for performance, especially if introducing new game entities or mechanics.
- **Collaboration**: Use feature branches and ensure thorough testing before raising a pull request.

---

Special thanks to **freecodecamp.org** for all the help and support into making this fun browser based web app.