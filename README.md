# Pomodoro Web

A zero-dependency, single-file pomodoro timer. No build step, no external assets — open `index.html` in any browser (or serve the folder with `python3 -m http.server`).

## Features

- **Focus / Short Break / Long Break** modes with a circular progress dial; long break after every N pomodoros (default 4).
- **Configurable** durations, long-break interval, auto-start, and desktop notifications via the Settings dialog. Settings and the daily completed count persist in `localStorage`.
- **Sound chime** on completion, synthesized with WebAudio (no audio files); toggle with the speaker button.
- **Accurate in background tabs** — the countdown is anchored to a wall-clock deadline, not interval ticks, so tab throttling can't drift it.
- **Keyboard shortcuts**: `Space` start/pause, `R` reset, `S` skip to the next phase.
- Light/dark theme follows the OS preference; the accent color shifts per mode (red focus, teal short break, blue long break).
- Ambient background: two blurred color fields drift slowly behind a frosted-glass card and re-tint with the active mode, plus a faint SVG grain texture. Pure CSS, honors `prefers-reduced-motion`.
