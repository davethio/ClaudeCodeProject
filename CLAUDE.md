# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A collection of browser-based games and web apps. No build system, bundler, or package manager — each app is a self-contained HTML file with inline CSS and JavaScript that runs by opening directly in a browser.

## Development

- **Run/preview:** Open any `.html` file directly in a browser (no server required).
- **No build step, no dependencies, no tests** — the project uses vanilla HTML/CSS/JS only.

## Architecture

Each game/app lives in a single `.html` file following this structure:
- `<style>` block for all CSS (dark theme, neon aesthetic)
- HTML markup for layout, canvas, and UI overlays
- `<script>` block for all game logic using Canvas 2D API

Games use a fixed-interval game loop (`setInterval`) with separate `update()` (state) and `draw()` (render) phases.

## Conventions

- All rendering uses the HTML5 Canvas 2D context.
- UI state changes (start screen, game over) are handled via a DOM overlay toggled with an `.active` CSS class.
- Grid-based coordinate system: positions stored as `{x, y}` cell indices, converted to pixels only at draw time.

## Version Control

- GitHub repo: https://github.com/davethio/ClaudeCodeProject
- Branch: `master`
- Commit all changes with descriptive messages and push to GitHub regularly.
