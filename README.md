# Reading Quest 2026

A gamified, pixel-art reading tracker for getting through 18 books by December 31, 2026.

## Features

- **Difficulty-weighted daily page targets** — harder books get fewer pages/day, easier ones get more, so every day feels like roughly the same effort
- **Sequential reading order** — set your order once, the app tracks which book you're on and what's next
- **Quick page logging** — tap +5/+10/+25/+50 buttons to log reading progress with pixel sparkle effects
- **GitHub auto-sync** — progress saves automatically to the repo via GitHub API, works across devices
- **Verification** — targets are checked to ensure all books finish within 2 days of the deadline
- **Edit mode** — update page counts, difficulty scores, add/remove books
- **Stats** — XP counter, streak tracking, estimated finish date, overall progress

## Design

Pokemon/pixel-art aesthetic with Press Start 2P font, retro beep sound effects (toggleable), and a dark blue-black color palette. Single `index.html` file with inline CSS and JS for easy GitHub Pages hosting.

## Usage

1. Open `index.html` in a browser (or host on GitHub Pages)
2. Hit **Calculate Targets** to generate daily page goals
3. Use **Order** to set your reading sequence
4. Log pages from the "Reading Now" card at the top
5. Click the **sync** indicator (top-right) to set up GitHub auto-sync

## Algorithm

Each book's "effort" = remaining pages x difficulty multiplier. Days are allocated proportionally by effort, then pages/day = remaining / allocated days. After rounding, targets are verified and adjusted so total reading time stays within 2 days of Dec 31, 2026.
