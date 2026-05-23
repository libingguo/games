# Games

A collection of browser-based games built with vanilla HTML, CSS, and JavaScript.

## Projects

### 1. Tic Tac Toe
A classic two-player Tic Tac Toe game with optional AI opponent.

**Features:**
- Two-player mode (local)
- Play against an unbeatable AI (minimax algorithm)
- Score tracking across games
- Smooth animations and modern UI
- Dark theme with retro styling

**How to Play:**
- Click cells to make your move
- Click the "vs Computer" button to toggle AI mode
- Click "New Game" to reset the board
- Scores persist across games

📄 **File:** `tictactoe.html`

---

### 2. Top-Down Shooter
A fast-paced top-down shooter game with pixel-art aesthetics and escalating difficulty.

**Features:**
- Arrow keys to move in 8 directions
- Mouse to aim, click to shoot
- 3 enemy types with unique behaviors:
  - **Grunt** (red): Direct charge, +10 points
  - **Flanker** (orange): Curved approach, +20 points
  - **Rusher** (purple): Fast zigzag movement, +30 points
- 5 progressively harder waves
- Score tracking and level progression
- Particle effects and muzzle flash
- CRT scanlines and starfield visual effects
- Health system (3 lives)

**How to Play:**
1. Click to start from the menu
2. Use **Arrow Keys** to move
3. Move your **mouse** to aim
4. **Left Click** to shoot (hold for continuous fire)
5. Defeat all enemies in a wave to progress to the next level
6. Complete all 5 waves to win
7. Press **R** or click to restart after game over

📄 **File:** `shooter.html`

---

## Getting Started

All games are self-contained HTML files. Simply download and open in any modern web browser:

```bash
# Tic Tac Toe
open tictactoe.html

# Top-Down Shooter
open shooter.html
```

No installation, dependencies, or server required.

---

## Browser Compatibility

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Any browser supporting HTML5 Canvas and ES6 JavaScript

---

## Technical Details

**Technologies:**
- HTML5 Canvas for rendering
- Vanilla JavaScript (no frameworks)
- CSS for styling and layout
- Responsive design (scales to window size)

**Game Loop:**
- `requestAnimationFrame` for smooth 60 FPS gameplay
- Input handling via keyboard and mouse events
- Collision detection using distance calculations
- Particle system for visual effects

---

## Future Ideas

- [ ] Sound effects and background music
- [ ] Leaderboard system
- [ ] Mobile touch controls
- [ ] Additional game modes
- [ ] Power-ups in the shooter
- [ ] Difficulty settings

---

## License

MIT License — feel free to use, modify, and distribute.

---

Enjoy the games! 🎮
