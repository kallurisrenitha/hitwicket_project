# hitwicket_project
Turn-based Chess-like Game with Websocket Communication given as a task from hitwicket
# Turn-Based Chess-Like Game with WebSocket Communication

## Overview

This project is a turn-based chess-like game where two players compete on a 5x5 grid using a team of characters with unique movement patterns. The game utilizes WebSocket communication for real-time interaction between clients and a server. Players can join or create rooms, make moves, and see updates instantly.

### Key Components

1. **Server**
   - Implements game logic.
   - Sets up a WebSocket server for real-time communication.
   - Processes game moves and maintains game state.

2. **WebSocket Layer**
   - Handles real-time communication between server and clients.
   - Manages game initialization, move commands, and state updates.

3. **Web Client**
   - Provides a web-based UI for the game board and controls.
   - Communicates with the server via WebSocket.
   - Renders game state and allows player interactions.

### Game Rules

#### Setup

- Played on a 5x5 grid.
- Each player controls a team of 5 characters:
  - **Pawn**: Moves one block in any direction. Commands: `L`, `R`, `F`, `B`.
  - **Hero1**: Moves two blocks straight. Commands: `L`, `R`, `F`, `B`.
  - **Hero2**: Moves two blocks diagonally. Commands: `FL`, `FR`, `BL`, `BR`.

#### Game Flow

- **Initial Setup**: Players deploy characters on their starting row.
- **Turns**: Players alternate turns, making one move per turn.
- **Combat**: Characters remove opponents from the game when they move into or through occupied spaces.
- **Invalid Moves**: Moves are invalid if they exceed bounds, are not allowed for the character, or target a friendly piece.

#### Winning

- The game ends when one player eliminates all of their opponent’s characters.

### Technical Requirements

1. **Server**
   - Implement core game logic and WebSocket server.
   - Process and validate moves, update game state, and broadcast updates.

2. **WebSocket Communication**
   - Handle events: game initialization, player moves, game state updates, invalid moves, and game over.

3. **Web Client**
   - Display a 5x5 game board and current game state.
   - Implement interactive features: clickable characters, move options, and game notifications.

### Implementation Steps

1. Set up the server with game logic.
2. Implement the WebSocket server.
3. Create the web client interface.
4. Integrate WebSocket communication.
5. Develop interactive features and game state rendering.
6. Finalize move validation, game flow, and UI improvements.

### Bonus Challenges

- Implement Hero3 with advanced movement.
- Add dynamic team composition and spectator mode.
- Integrate chat features and AI opponents.
- Create a replay system and ranking system.

### Setup Instructions

#### Prerequisites

- Node.js (for server-side WebSocket implementation)
- Any modern web browser

#### Server Setup

1. Clone the repository:
   ```sh
   git clone <repository-url>
   cd <repository-folder>
