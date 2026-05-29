# AGENTS.md

## Project Overview

This repository contains **地牢幸存者 · Dungeon Survivor**, a small browser roguelite game inspired by Vampire Survivors. The game is implemented as a static single-page HTML app using Canvas and plain JavaScript.

Primary files:

- `index.html` - game UI, styling, Canvas rendering, input handling, and gameplay logic.
- `hero.png` - player sprite sheet.
- `grub.png` / `runner.png` - enemy sprite sheets.
- `README.md` - user-facing description and local run instructions.

## Local Run

No build step is required.

Open `index.html` directly in a browser, or run a simple static server from the repository root:

```bash
python3 -m http.server 8000
```

Then visit:

```text
http://localhost:8000
```

## Development Notes

- Keep the project dependency-free unless there is a strong reason to add tooling.
- Prefer editing `index.html` directly; the current architecture intentionally keeps the game in one file.
- Preserve mobile support. The game uses touch input and viewport-sized Canvas rendering.
- Preserve keyboard support. Movement should continue to work with `WASD` and arrow keys.
- Keep asset paths relative to `index.html` so GitHub Pages and local static servers work the same way.
- Avoid large unrelated rewrites when tuning balance, UI, or gameplay. This makes small gameplay changes easier to review.

## Testing Checklist

After changing gameplay, input, layout, or assets, verify at least:

- The game starts from the title screen.
- Player movement works with keyboard on desktop.
- Touch/drag movement works on mobile or a mobile viewport.
- Pause and resume work with the pause button and `P` / `Esc`.
- Enemies spawn, move toward the player, take damage, and drop experience.
- Level-up choices appear and apply correctly.
- Game over and retry reset the run cleanly.

For quick browser testing, use:

```bash
python3 -m http.server 8000
```

## Style Guidelines

- Use plain JavaScript and browser APIs already present in the file.
- Keep functions small enough to scan, but avoid introducing framework-style abstractions.
- Use concise comments for non-obvious game logic, especially balance rules and collision behavior.
- Match the existing Chinese UI copy style when adding visible text.
- Keep CSS responsive and avoid fixed layouts that break on narrow mobile screens.

## Git Hygiene

- Do not overwrite user changes in `index.html` or image assets.
- Keep commits focused on one gameplay, UI, balance, or documentation change at a time.
- Do not add generated build artifacts; this project should remain directly runnable from source.
