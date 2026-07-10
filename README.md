# Tic-Tac-Toe Web Application

A responsive Tic-Tac-Toe game built with vanilla HTML, CSS, and JavaScript — no frameworks or libraries.

## Features

- **Two game modes**: 2-Player (pass and play) or vs. AI
- **Simple AI opponent**: prioritizes winning moves, then blocks the opponent, then takes center/corner/random cells
- **Win detection**: checks all 8 winning lines (rows, columns, diagonals) plus draw detection
- **Score tracking**: running tally of X wins, O wins, and draws across rounds
- **Visual feedback**: cell pop-in animation on placement, glowing highlight on the winning line
- **Accessible**: `role="gridcell"` / `aria-label` on cells, respects `prefers-reduced-motion`
- **Fully responsive**: board scales with viewport using `clamp()` and `aspect-ratio`

## Tech Stack

- HTML5
- CSS3 (custom properties, grid layout, keyframe animations)
- Vanilla JavaScript (ES6+, no dependencies)

## How It Works

- `board` is a 9-element array representing cell state (`null`, `'X'`, or `'O'`)
- `checkWinner()` compares the board against 8 predefined winning line combinations
- `handleMove()` handles a click: places the mark, checks for a winner, switches turns, and triggers the AI if enabled
- `aiMove()` implements a lightweight heuristic (not full minimax): win → block → center → corner → random

## Running Locally

Just open `index.html` in any browser — no build step or server required.

## Possible Extensions

- Upgrade the AI to full minimax for an unbeatable opponent
- Add a match history log
- Add sound effects / haptic feedback
- Persist scores with localStorage
