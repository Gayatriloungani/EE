2048 — Functional Implementation (React)

A functional, modular implementation of the classic 2048 game with a dynamic GUI.
This repository contains a configurable Y×Y board (default 4×4), functional-style game logic, score tracking, keyboard and swipe controls, and all features required to play and restart the game. The app is written as a React web app using functional components and pure, testable game logic.

Table of Contents

Features

Tech & Design Choices

Installation & Run (Local)

Build & Deploy

Gameplay & Controls

Configuration

Implementation Details

Project Structure

Testing

Contributing

License

Features

Default board size: 4×4 (configurable to any Y×Y).

Start with two random tiles (value 2 or 4).

Slide tiles up / down / left / right using keyboard or GUI controls.

Matching tiles merge to their sum (e.g., 2 + 2 = 4).

After every valid move, a new tile (2 or 4) spawns in a random empty cell.

Win condition: when a tile reaches 2048.

Lose condition: when no valid moves remain.

Tracks and displays score based on merged tiles.

Restart button in GUI.

Pure, functional logic for game state and moves (easy to test & reuse).

Modular codebase — UI separated from game logic.

Tech & Design Choices

Framework: React (functional components & hooks)

Language: JavaScript (ES6+). TypeScript optional (recommended for production).

Styling: CSS modules / Tailwind (optional)

Architecture:

Game logic implemented as pure functions (no side effects): moveLeft, moveRight, moveUp, moveDown, mergeRow, spawnRandomTile, hasMoves, etc.

UI uses React state (useReducer or useState) and dispatches results from pure functions.

Clear separation: src/game (logic) and src/ui (components).

Deployment: GitHub Pages, Vercel, Netlify, or any static host.

Installation & Run (Local)
Prerequisites

Node 18+ and npm (or pnpm/yarn)

Git

Clone & Run
# clone repo
git clone https://github.com/<Gayatriloungani>/EE.git
cd Exponent_energy

# install dependencies
npm install

# start dev server
npm start


Open http://localhost:3000 (or the port printed in terminal).

Build & Deploy
Build
npm run build


This produces a build/ folder ready for deployment.

Deploy to GitHub Pages (example)

Install gh-pages:

npm install --save-dev gh-pages


Add to package.json:

"homepage": "https://<Gayatriloungani>.github.io/EE",
"scripts": {
  "predeploy": "npm run build",
  "deploy": "gh-pages -d build"
}


Deploy:

npm run deploy
