# AGENTS.md

Vanilla HTML5 Canvas Asteroids clone. Single-file game (`game.js`), no dependencies, no bundler, no build.

## Run

Open `index.html` directly in a browser, or `npx serve .` then visit `http://localhost:3000`.

## Verify

No tests, linter, or typecheck exist. Verify by running the game in a browser (`game.js` throws in the console on obvious issues; there is no other check).

## Conventions

- All UI strings, comments, and `index.html` content are in **Spanish** (`lang="es"`). Keep new strings in Spanish. JS identifiers are English.
- Do not convert to ES modules/imports or add a bundler — `index.html` loads `game.js` via a plain `<script>` tag and `game.js` relies on script-tag globals, `'use strict'`, and module-level singletons (`ctx`, `W`/`H` constants, game state).
- Keep everything in `game.js`; visual style is stroke-only white-on-black (`#fff` lines on `#000` background), monospace HUD.
- Screen is fixed at 800x600 (`W`/`H` constants); wrap-around uses the `wrap(v, max)` helper.