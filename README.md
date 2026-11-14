# OUTPOST ZERO — Junior Astronaut Mission Trainer

A browser-playable Mars outpost management game for the 2026 NASA Space Apps Challenge.

**Status:** Early playable prototype. The mission loop, resource controls, simplified system interactions, debrief, and optional NASA DONKI SEP lookup are implemented in `index.html`.

## Run locally
Open `index.html` in a modern browser. No build step, package install, or server is required. The game works offline; the optional NASA DONKI lookup requires an internet connection.

## Publish with GitHub Pages
1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch **main** and folder **/ (root)**, then save.
4. Wait for GitHub Pages to publish, then open the URL shown on the Pages settings screen.
5. Test the link in a private/incognito window and on a phone.

## Project files
- `index.html` — the game.
- `PROJECT_RULES.md` — instructions for coding agents and contributors.
- `SCIENCE.md` — NASA sources, interpretation limits, and simulation assumptions.

## Science note
NASA DONKI provides real space-weather records. The game uses a returned SEP record as context for a simulated shelter drill. It does **not** turn that record into a Mars radiation dose. All game resource units and consequences are simplified educational values. Check `SCIENCE.md` and verify the exact challenge Resources list before submission.

## AI-use disclosure
Update this section before submission to name every AI/SI tool used, what it contributed (for example: code generation, debugging, text, or visuals), and what the team reviewed or changed. Do not claim that AI-generated work was created entirely by the team without assistance.

## Team
Add all six team members and their roles before submission.

## License
No license has been selected yet. Until one is added, do not assume others have permission to reuse the code.

## Mission flow and one-shot setup tasks
1. The five-person crew lands at Gale Crater and surveys the outpost site.
2. The captain assigns four specialists to power, life support, food production, and radiation-protection setup.
3. Each setup task has a distinct minigame and one attempt. A failed result is locked for that mission; there is no task retry.
4. Failed setup leaves a persistent system problem. During the seven Sols, the captain compensates by reallocating power among maintenance, life support, greenhouse production, and shelter protection.
5. A full new mission resets the task results and starts a fresh run.
