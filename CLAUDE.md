# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Running the Games

No build step, server, or dependencies required. Open either file directly in a browser:

```bash
open tictactoe.html   # macOS
xdg-open tictactoe.html   # Linux
# or just double-click the file in a file manager
```

## Architecture

Both games are fully self-contained single-file HTML documents (HTML + CSS + JS in one file). There is no package manager, bundler, or external dependency.

### tictactoe.html

Module-level variables hold all state (`board[]`, `current`, `gameOver`, `vsComputer`, `scores`). The AI uses minimax — `bestMove()` calls `minimax()` recursively to find the optimal `O` move. The eight winning combinations are declared once as `WINS` and reused by both `checkWinner()` and the minimax scorer.

### shooter.html

Object-oriented design with five classes: `Game`, `Player`, `Enemy`, `Bullet`, `Particle`. The `Game` class owns all collections (`bullets`, `enemies`, `particles`) and drives the `requestAnimationFrame` loop via `Game.loop()`.

Game state is a simple integer enum (`STATE.MENU | PLAYING | LEVEL_CLEAR | GAME_OVER | VICTORY`). Wave progression is controlled by a shuffled `queue[]` array; enemies spawn one at a time on a `spawnT` countdown. The five waves are declared in the `WAVES` constant array.

The canvas is fixed at 800×600 and scaled to the window via `canvas.style.width/height` (CSS scaling, not canvas resolution scaling). Enemy speed scales with level via a `m = 1 + (level-1)*0.2` multiplier applied at construction time.

Player supports both arrow keys and WASD. Mouse position is tracked in a `mouse` object and used for both aiming and shooting.
