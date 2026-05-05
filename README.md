# ⚡ NEON-NEXUS: QUANTUM GRID ⚡

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero-brightgreen?style=for-the-badge)

**Neon-Nexus** is a hyper-futuristic, cyberpunk reimagining of Tic-Tac-Toe. It strips away the staleness of the classic game by introducing a **"Quantum Memory"** twist, creating a continuous, high-tension strategy battle. 

Built entirely in a **single HTML file** with zero external libraries, frameworks, or media assets. Everything from the particle explosions to the synthesizer sound effects and AI voice lines is generated procedurally in your browser.

---

## 🎮 The "Quantum" Twist

This is not your standard grid. **You can only have 3 active nodes (pieces) on the board at any time.** 

When you place your 4th node, your 1st (oldest) node *glitches out of existence* and disappears from the board. This forces players to constantly think several moves ahead, managing their node lifespan while trying to trap their opponent. 

> **Warning:** The piece about to collapse will become unstable and pulse on the grid. Plan accordingly.

---

## ✨ Features

* **🧠 Hardcore AI Opponent:** A custom implementation of the **Minimax Algorithm with Alpha-Beta Pruning**, specifically modified to understand and anticipate the disappearing "Quantum" pieces. It will set traps and block your wins flawlessly.
* **🔊 Procedural Web Audio Synth:** No `.mp3` files needed. Every sound effect (placing pieces, glitches, victory themes, timeouts) is synthesized live using the browser's native `AudioContext` API.
* **🗣️ AI Voice Announcer:** Utilizes the native `SpeechSynthesis` API to narrate the match, taunt the player, and announce grid collapses.
* **💥 "Juicy" Game Feel:** Features screen shake, time-limit penalties, and a custom 60fps HTML5 Canvas particle engine for node explosions.
* **🕶️ Cyberpunk UI:** Heavy use of CSS glassmorphism, CRT scanline overlays, chromatic aberration, and dynamic neon glowing effects.
* **🔌 Zero Dependencies:** 100% Vanilla HTML, CSS, and JS. 

---

## 🕹️ How to Play

1. **Clone or Download** the repository.
2. Open `game.html` in any modern web browser (Chrome, Edge, Firefox, Safari).
3. **Turn your volume up** to hear the procedural synth and AI voice lines.
4. Click **INITIALIZE SYSTEM** to start.
5. Choose between **Multiplayer (Local)** or **Vs AI (Hardcore)**.
6. Connect 3 in a row to win, but remember: *your 4th move deletes your 1st!*

---

## 💻 Tech Stack & Mechanics

### Single-File Architecture
The entire application is self-contained. The styling, game state logic, canvas rendering loop, and audio generation all live within `index.html`.

### The AI Algorithm (Minimax)
Standard Tic-Tac-Toe has 255,168 possible games. The Quantum twist creates a near-infinite loop of states. To make the AI viable without freezing the browser, the Minimax algorithm is bounded by a **depth limit** and uses **alpha-beta pruning** to ignore mathematical branches that yield worse outcomes than the current best path. The AI simulates the board, tracks the array of piece histories, removes the oldest simulated piece when necessary, and scores the board state.

### Procedural Particle Engine
A lightweight, custom 2D physics engine runs on a `<canvas>` layered behind the UI. When a piece is placed or destroyed, the engine generates `Particle` objects with velocity, gravity, and decay properties, rendering them with a glow effect (`shadowBlur`).

---

## 🚀 Future Roadmap

- [ ] Online Multiplayer via WebSockets / Socket.io.
- [ ] Mobile touch optimization and PWA support.
- [ ] Additional AI difficulty levels.
- [ ] Leaderboards and win-streak tracking.

---


*Good luck. The grid is waiting.*
