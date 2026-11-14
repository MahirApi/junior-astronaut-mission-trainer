# Project rules — OUTPOST ZERO

## Goal
Build a polished, browser-playable educational Mars outpost simulator for the 2026 NASA Space Apps Challenge, aimed primarily at learners aged 7–12.

## Working style (PONYTAIL)
- Read the existing code before changing it.
- Make the smallest complete change that solves the task.
- Reuse existing patterns and browser APIs; do not add a framework or dependency without a strong reason.
- Do not add speculative features or abstractions.
- Preserve accessibility, validation, error handling, and honest science attribution.
- For non-trivial logic, include a small self-check or test.
- State what was skipped or not checked and disclose important risks.

## Product constraints
- Keep the experience easy to understand for a first-time young player.
- The four challenge systems must affect one another: power, life support, radiation protection, and food production.
- Decisions must have understandable consequences. No fake precision.
- Clearly distinguish NASA observations from the game's simplified training model.
- Never claim a model output is measured NASA telemetry.
- Do not use NASA logos, insignia, mission patches, or other NASA branding in generated artwork.
- Keep the app playable without an API response. Live data is an enhancement, never a hard dependency.
- No secrets or API keys in the repository. NASA DEMO_KEY may be used for low-volume development only; do not rely on it for a public launch.

## Architecture
- The initial prototype is a self-contained `index.html` using browser-native HTML, CSS and JavaScript.
- Avoid build tools and external dependencies unless the team explicitly chooses to add them.
- Keep scientific references and assumptions documented in `SCIENCE.md`.
- Update the README whenever the run instructions, data sources, or deployment steps change.

## Definition of done
1. A first-time player can start, complete or fail a mission, and understand the debrief.
2. The four core systems have visible, interconnected effects.
3. NASA data failures degrade gracefully to a clearly labelled training scenario.
4. The app works on a clean desktop browser and a mobile-width viewport.
5. Data sources, model assumptions, and AI usage are disclosed in the submission.
6. Test all changed flows before declaring the work complete.
