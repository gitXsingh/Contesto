# CONTESTO
Instant LeetCode-style contests. Generate a fresh set of problems by difficulty, start a timer, track solved items, and toggle dark mode — all in a clean, responsive UI.

Demo: https://gitxsingh.github.io/Contesto/

## ✨ Features
- **One-click contest**: Auto-picks 1 Easy, 2 Medium, 1 Hard from `data/questions.json`
- **Timer built-in**: Set your own duration and get a simple countdown
- **Mark as solved**: Toggle solved state inline
- **Regenerate anytime**: Get a fresh set of problems instantly
- **Dark mode**: Sun/Moon toggle with system preference + persistence
- **Lightweight**: Pure HTML/CSS/JS; no frameworks required

## 🚀 Quick Start
Because the app loads `data/questions.json`, you should run it via a local server (browsers block `fetch` from file://).

- Windows PowerShell (Python 3):
  ```bash
  cd D:\PROJECTS\Contesto
  python -m http.server 5500
  # Open: http://localhost:5500/
  ```
- Or use any static server (Node, VS Code Live Server, etc.).

## 🧭 Usage
1. Open the app and set “Contest Duration (minutes)”
2. Click “Start Contest”
3. Work through the links:
   - Easy → Medium → Hard
   - Click “Mark as Solved” per question
4. Need a new set? Use “Regenerate Contest”
5. Stop anytime with “End Contest”
6. Toggle theme via the top-right Sun/Moon button

## 🧩 Customization
- **Change problem set**: Edit `data/questions.json`
  - Each item should have `title`, `titleSlug`, and `difficulty` (`EASY|MEDIUM|HARD`)
  - Links are built as `https://leetcode.com/problems/{titleSlug}/`
- **Default timer**: Controlled in `js/main.js` (defaults to 60)
- **Styling**: Colors are theme variables in `css/styles.css` (`:root` and `[data-theme="dark"]`)
- **Branding**: Top-left brand text and font live in `index.html` and `css/styles.css`

## 🗂️ Project Structure
```text
Contesto/
├─ index.html          # App shell and UI elements
├─ css/
│  └─ styles.css       # Theme variables, layout, components
├─ js/
│  └─ main.js          # Contest logic, timer, UI rendering, theme toggle
└─ data/
   └─ questions.json   # Problem dataset (E/M/H)
```

## ♿ Accessibility
- High-contrast dark mode
- Icon toggle with `aria-label` and `aria-pressed`
- Focus-visible and color variables for readability

## 🛣️ Roadmap Ideas
- Persist solved state per session
- Customizable counts per difficulty
- Difficulty badges in UI (not only color)
- Keyboard shortcuts (start/regenerate/end)
- Export/Share contest set

## 🧪 Tech Stack
- HTML5, CSS3, Vanilla JavaScript

## 📝 License
MIT © 2025
