# BrainwavesHTML

BrainwavesHTML is a single-page web application for experimenting with isochronic brainwave audio. It uses the Web Audio API to generate an audible carrier tone, pulse it at a selected brainwave frequency, and optionally blend in ambient noise for a softer listening experience.

The app runs entirely in the browser from `index.html` and uses CDN-hosted Tailwind CSS and Lucide icons for styling and interface icons.

> **Note:** This project is for audio experimentation and relaxation/focus workflows only. It is not medical advice, a medical device, or a substitute for professional care.

## Getting Started

No build step is required. Open the app directly in a modern browser:

```bash
open index.html
```

If your browser restricts local files, serve the repository with any static web server instead:

```bash
python3 -m http.server 8000
```

Then visit <http://localhost:8000>.

## Basic Controls

- **Start/Stop Entrainment:** Starts or stops the generated audio session.
- **Pulse Frequency (Hz):** Sets the modulation frequency used for the isochronic pulse.
- **Presets:** Quickly select common targets: Sleep (2 Hz), Meditate (6 Hz), Relax (10 Hz), Alert (20 Hz), and Focus (40 Hz).
- **Carrier Pitch (Hz):** Changes the audible base tone that carries the pulse.
- **Tone Type:** Switches the carrier waveform between sine, triangle, and square.
- **Pulse Style:** Changes the modulation shape between smooth sine pulses and sharper square pulses.
- **Volume:** Controls the master output level.
- **Ambient Noise:** Blends in white, pink, or brown-style filtered noise.
- **Session Timer:** Stops playback automatically after 15, 30, or 60 minutes, or runs indefinitely until stopped manually.

## Development

This repository currently contains a lightweight static app:

- `index.html` — application markup, styling, and JavaScript.
- `README.md` — project overview and usage notes.
- `LICENSE` — MIT license terms.
- `AGENTS.md` — guidance for future AI coding agents.

Because the app is static, most changes can be validated by opening `index.html` in a browser and testing the controls manually.

## Roadmap

- Add saved user presets for favorite frequency, pitch, noise, and timer combinations.
- Add a visual frequency guide explaining common delta, theta, alpha, beta, and gamma ranges.
- Add keyboard shortcuts and improved accessibility labels for all controls.
- Add optional offline/local copies of UI dependencies.
- Add automated smoke tests for the main control flow.
