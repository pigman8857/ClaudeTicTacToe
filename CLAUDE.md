# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This repository contains browser-based games implemented as self-contained single HTML files — no build step, no dependencies, no server required.

## Running the Games

Open any HTML file directly in a browser:

```bash
xdg-open tictactoe.html
xdg-open invader.html
xdg-open dinosaur.html
```

Or navigate to the file via `file:///home/somkamolv/Documents/Dev/ClaudeCodeTest/<filename>.html`.

## Architecture

Each game is a **single `.html` file** containing inline `<style>`, `<canvas>` or DOM elements, and `<script>`. There are no external dependencies, frameworks, or assets.

- **`tictactoe.html`** — 2-player local Tic Tac Toe. Uses DOM grid cells, tracks scores across rounds.
- **`invader.html`** — Space Invaders clone. Uses `<canvas>` with a `requestAnimationFrame` game loop. Player moves with `←`/`→`, shoots with `Space`. Invaders (magenta/yellow/cyan rows) march downward and speed up as they are destroyed.
- **`dinosaur.html`** — Dinosaur sidescroller. Uses `<canvas>` with a `requestAnimationFrame` game loop. Mash `Space` to control speed (rolling 1s window of keypresses maps to 60–800 px/s). Reach the apple at world position 3920 within 10 seconds. Legs animate faster at higher speed. Press `R` to restart.

## Remote

GitHub repository: `https://github.com/pigman8857/ClaudeTicTacToe` (branch: `main`)
