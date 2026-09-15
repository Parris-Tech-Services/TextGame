# TextGame

A zero-dependency browser text-adventure engine with a complete playable demo: **Signal at Black Ridge**.

## What works

- deterministic command parser with aliases (`n`, `e`, `look`, `take`, `use`, `rest`, etc.)
- immutable game-state transitions that are easy to test
- autosave to browser `localStorage`
- one-step undo for state-changing actions
- keyboard-first terminal plus large phone-friendly quick commands
- health, stamina, inventory, discovered locations and a real win condition
- offline app shell through a service worker
- Node regression tests and GitHub Actions CI
- GitHub Pages deployment from `main`

## Run locally

Any static server works. For example:

```bash
python -m http.server 8080
```

Then open `http://localhost:8080`.

## Test

```bash
npm test
```

The engine lives in `src/engine.mjs`; the DOM adapter lives in `src/app.mjs`. Keeping those separate lets game rules stay deterministic and testable.
