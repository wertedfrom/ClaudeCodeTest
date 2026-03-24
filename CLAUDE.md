# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A collection of browser-based games implemented as self-contained single-file HTML applications. Each game bundles its own HTML, CSS, and JavaScript with no external dependencies or build system.

## Running

Open any `.html` file directly in a browser. No build step, server, or package manager required.

## Architecture

- **tictactoe.html** — Two-player tic-tac-toe with score tracking. Uses DOM elements for the grid, inline `<style>` and `<script>`.
- **shooter.html** — Retro top-down shooter using HTML5 Canvas. All game logic runs in a single `<script>` block organized into labeled sections (Configuration, Sprite Generation, Game State, etc.). Key design points:
  - `CONFIG` object at the top controls all tunable game parameters (speeds, sizes, timings).
  - `PALETTE` and `ENEMY_TYPES` objects define visual theming and enemy variants (basic, fast, tank).
  - Sprites are procedurally generated at startup from pixel arrays via `createSprite()`, not loaded from image files.
  - Game loop uses `requestAnimationFrame`.

## Workflow

- Commit work to git frequently with clean, descriptive commit messages. Push to GitHub regularly so progress is never lost.
- Commit at natural checkpoints: after completing a feature, fixing a bug, or reaching a stable state.

## Conventions

- Each game is fully self-contained in a single HTML file — no shared code, no external assets.
- Dark color scheme (`#1a1a2e` / `#0a0a1a` backgrounds) across both games.
