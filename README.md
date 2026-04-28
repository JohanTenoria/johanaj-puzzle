# 🔢 Number Tapper

<div align="center">

![Number Tapper Banner](https://img.shields.io/badge/Puzzle-Sliding%20Game-5ee7df?style=for-the-badge)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

**A sleek, challenging sliding puzzle game with multiple difficulty modes, hints, undo, and leaderboards.**

[Play Now](https://your-username.github.io/number-tapper) · [Report Bug](issues-link) · [Request Feature](issues-link)

</div>

---

## 📖 About

Number Tapper is a modern take on the classic 15-puzzle (sliding puzzle) where you must arrange numbered tiles in ascending order by sliding them into the empty space. Features multiple difficulty levels, time pressure modes, locked tiles, and a persistent scoreboard.

Built with vanilla HTML/CSS/JS — no frameworks, no dependencies, just smooth animations and clean code.

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🎮 **4 Difficulty Modes** | Easy (4x4), Hard (5x3 locks), Expert (6x5 locks + timer), Nightmare (7x8 locks + timer) |
| 🔒 **Locked Tiles** | Strategic obstacles that cannot move — plan your route! |
| ⏱️ **Timed Mode** | Race against the clock in Expert and Nightmare difficulties |
| 💡 **Smart Hints** | Suggests the optimal next move using Manhattan distance heuristic |
| ↩️ **Undo History** | Reverse up to 60 moves (perfect for learning) |
| 👁️ **Preview Mode** | See where each tile needs to go (goal coordinates) |
| 🏆 **Persistent Scoreboard** | Top 50 scores saved locally with difficulty filtering |
| ⌨️ **Keyboard Support** | Arrow keys / WASD to control the empty space |
| 📱 **Fully Responsive** | Plays beautifully on desktop, tablet, and mobile |
| ✨ **Smooth Animations** | GPU-accelerated tile sliding with CSS transforms |

---

## 🎯 How to Play

1. **Objective**: Arrange tiles from 1 to N (where N = board size² - 1) in ascending order, left to right, top to bottom.
2. **Rules**: 
   - Only tiles adjacent to the empty space can slide into it
   - Locked tiles (🔒) cannot move — work around them
   - In timed modes, solve before the clock hits zero
3. **Controls**:
   - **Click** a tile to slide it toward the empty space
   - **Arrow keys / WASD** to move the empty space (inverted logic for pro players)
   - **Hint** button shows the best next move
   - **Undo** reverses your last move
   - **Preview** shows target coordinates on each tile

---

## 🎮 Difficulty Modes

| Mode | Size | Shuffle Depth | Locked Tiles | Hints | Timer | Target Audience |
|------|------|---------------|--------------|-------|-------|-----------------|
| 🟢 **Easy** | 4x4 | 80 | 0 | 5 | None | Beginners |
| 🟡 **Hard** | 5x5 | 200 | 3 | 3 | None | Casual players |
| 🟣 **Expert** | 6x6 | 400 | 5 | 2 | 5:00 | Puzzle enthusiasts |
| 🔴 **Nightmare** | 7x7 | 600 | 8 | 1 | 3:00 | Masochists |

**Ranking System**:
- **S-Rank** 🏆: 0 hints used, moves < size × 20
- **A-Rank** 🥇: 1 hint used
- **B-Rank** 🥈: 2 hints used  
- **C-Rank** 🥉: 3+ hints used

---

## 🛠️ Technical Details

### Stack
- **Pure HTML5** — Semantic structure
- **CSS3** — CSS Grid, CSS Variables, GPU-accelerated transforms, responsive design
- **Vanilla JavaScript ES6+** — No dependencies, ~400 lines of clean code

### Key Algorithms
- **Manhattan Distance Heuristic** — Used for intelligent hints
- **Random Walk Shuffling** — Ensures puzzle solvability (with depth parameter)
- **Local Storage Persistence** — Scores saved across browser sessions

### Performance Optimizations
- `will-change: transform` for smooth animations
- Tile recycling (no DOM thrashing on render)
- Debounced animation queue to prevent move stacking
- CSS transitions instead of JS animations

---

## 📦 Installation

```bash
# Clone the repository
git clone https://github.com/your-username/number-tapper.git

# Navigate to project
cd number-tapper

# Open in browser (any modern browser works)
open index.html

# Or serve locally
python -m http.server 8000
# Then visit http://localhost:8000
