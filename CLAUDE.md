# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This repository contains browser-based games and miscellaneous HTML files implemented as self-contained single HTML files — no build step, no dependencies, no server required.

---

## Games

### Running the Games

Open any HTML file directly in a browser:

```bash
xdg-open tictactoe.html
xdg-open invader.html
xdg-open dinosaur.html
```

Or navigate to the file via `file:///home/somkamolv/Documents/Dev/ClaudeCodeTest/<filename>.html`.

### Architecture

Each game is a **single `.html` file** containing inline `<style>`, `<canvas>` or DOM elements, and `<script>`. There are no external dependencies, frameworks, or assets.

- **`tictactoe.html`** — 2-player local Tic Tac Toe. Uses DOM grid cells, tracks scores across rounds.
- **`invader.html`** — Space Invaders clone. Uses `<canvas>` with a `requestAnimationFrame` game loop. Player moves with `←`/`→`, shoots with `Space`. Invaders (magenta/yellow/cyan rows) march downward and speed up as they are destroyed.
- **`dinosaur.html`** — Dinosaur sidescroller. Uses `<canvas>` with a `requestAnimationFrame` game loop. Mash `Space` to control speed (rolling 1s window of keypresses maps to 60–800 px/s). Reach the apple at world position 3920 within 10 seconds. Legs animate faster at higher speed. Press `R` to restart.

---

## Other Files

- **`test_pr.html`** — Static page with a cyan/magenta/yellow gradient background and centered "This is Pigman8857" text. Created on branch `feature/test_pr` as a PR test, pending merge to `main`.

### Serving Files Locally

To serve files over HTTP (useful for testing):

```bash
python3 -m http.server 8080 --directory /home/somkamolv/Documents/Dev/ClaudeCodeTest
```

Then open `http://localhost:8080/<filename>.html` in a browser. Stop the server with `kill $(lsof -ti:8080)`.

---

## Remote

GitHub repository: `https://github.com/pigman8857/ClaudeTicTacToe` (branch: `main`)
