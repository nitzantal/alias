# Notes for Claude

## Testing UI and configurable code

Whenever you write a UI with several buttons, inputs and controls, or code driven by a config file with many parameters and flags, verify every control and every option, not just the main flow. Click each button in each direction (for example both + and −, at the minimum and maximum), try each mode and each flag value, and check the resulting state and what is displayed. Run it in a real browser or the real runtime when possible. Do not report it as working until each one has been exercised.

Origin: in an Alias game a generic "stepper" control was tested only on numeric settings, and the "number of teams" + button (which acts on an array) produced NaN. No test had clicked that button.

## Project notes

- Static site published with GitHub Pages from `main` (root). No build step.
- When changing any JS/CSS file, bump the `?v=N` suffix on all assets in `index.html` so browsers do not serve stale cached files.
- Word bank defaults live in `words-alias-he.js`; user edits are stored in the browser's localStorage.
