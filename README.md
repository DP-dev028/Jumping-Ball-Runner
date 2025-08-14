# Jumping Ball Runner

A tiny, colorful, one-file runner game. Boing over goofy obstacles, enjoy parallax skies, and chase your high score — with zero installs and funny procedural sounds.

## Features
- Increasing speed and escalating challenge
- Distance-based scoring with persistent High Score (localStorage)
- Retry and Mute buttons, plus keyboard and touch controls
- Parallax backgrounds (clouds + rolling hills)
- Cartoonish ball and animated obstacles (boxes and spikes)
- No assets, no build — single HTML file, offline-friendly
- Fun procedural sounds for jump, crash, milestones, and start

## Controls
- Jump: Space / Up Arrow / Tap or Click
- Retry: R (or the Retry button after a crash)
- Mute: M (or the speaker button)

Tip: Time your jumps late — the boing is strong!

## How to Run
1. Save the HTML from this repo as “jumping-ball-runner.html”.
2. Open it in a modern browser (Chrome, Edge, Firefox, Safari).

Optional: Serve it locally
- Python: `python -m http.server`
- Node: `npx serve`

Deploy anywhere that serves static files (GitHub Pages, Netlify, Vercel, etc.).

## Gameplay
- Objective: Survive as long as possible by jumping over obstacles.
- Speed ramps up over time; the world scrolls faster the longer you live.
- Score increases with distance; milestone chimes play at nice round numbers.
- High score is saved across sessions (localStorage).

Forgiveness built-in:
- Coyote time (tiny grace period after leaving the ground)
- Jump buffer (tiny grace period if you jumped just before landing)

## Technical Notes
- HTML5 Canvas for rendering; Web Audio API for sounds
- Fully self-contained single file; no external assets or libraries
- Responsive layout; uses Pointer Events for touch input

If you don’t hear sound, interact once (tap/click) to unlock audio — browsers require a user gesture.

## Customize / Tuning
Open the file and tweak a few friendly constants:
- Difficulty:
  - state.accel (speed ramp), state.maxSpeed (maximum speed)
  - player.gravity and player.jumpV (jump feel)
- Aesthetics:
  - CSS variables in :root control colors and UI accents
- Spawning:
  - The spawn interval scales with speed; adjust the base formula in update()

## Accessibility & Privacy
- Keyboard and touch friendly; UI buttons are labeled.
- High-contrast, colorful visuals; screen reader support is minimal due to the real-time canvas.
- No tracking, no network calls. Stores high score only (localStorage).

## Troubleshooting
- No audio? Click/tap the game once; then toggle sound with M.
- High score not saving? Check browser storage permissions or private mode.
- Performance: Close extra tabs; reduce display scale; try another browser if needed.

## License
MIT — reuse, remix, and have fun. Attribution appreciated but not required.

Enjoy the run — and may your boings be perfectly timed! 🎈
