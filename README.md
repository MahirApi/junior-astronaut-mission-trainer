# OUTPOST ZERO — Junior Astronaut Mission Trainer

A browser-playable Mars outpost management game for the 2026 NASA Space Apps Challenge.

**Status:** Expanded playable prototype. The game now includes a knowledge preflight, adaptive manual landing challenge, three selectable Mars training sites, four adaptive one-shot commissioning minigames, a 30-Sol campaign, seven major crises plus seven captain-decision incidents, a shared power budget, three repair kits, two field-operation slots per Sol, hands-on panel cleaning, rover navigation, relay wiring, sample analysis, cadet XP/levels/badges, and an optional NASA DONKI SEP lookup in `index.html`.

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
NASA DONKI provides real space-weather records. The game uses a returned SEP record as context for a simulated Sol 23 shelter drill. It does **not** turn that record into a Mars radiation dose. Dust, filter, crop, pressure-seal, storm and heater incidents are authored game scenarios, not NASA forecasts. All game resource units and consequences are simplified educational values. Check `SCIENCE.md` and verify the exact challenge Resources list before submission.

## AI-use disclosure
Update this section before submission to name every AI/SI tool used, what it contributed (for example: code generation, debugging, text, or visuals), and what the team reviewed or changed. Do not claim that AI-generated work was created entirely by the team without assistance.

## Team
Add all six team members and their roles before submission.

## License
No license has been selected yet. Until one is added, do not assume others have permission to reuse the code.

## Mission flow
1. A five-question knowledge check establishes a practice, standard or advanced starting tier for piloting, engineering, life support, botany and science. It is a game difficulty setting, not a formal assessment of a child's ability.
2. Choose Gale Crater, Jezero Crater or Utopia Planitia. Each route has a small, clearly described gameplay modifier; these are scenario presets, not claims that a real mission should land at a particular place.
3. Complete a six-turn landing simulator. Engine thrust affects descent speed; steering offsets crosswind. A hard landing causes persistent equipment damage and consumes a spare kit.
4. Assign four specialists to the power, life-support, food-production and radiation-protection setup tasks. Each has one adaptive minigame attempt. Failed outcomes remain in the run.
5. Manage 30 Sols through a shared power budget, persistent allocations and three spare repair kits.
6. Major crisis beats arrive on Sols 3, 7, 11, 15, 19, 23 and 27. Additional captain-decision incidents on Sols 5, 9, 13, 17, 21, 25 and 29 ask the player to trade water, battery, food, crew safety, science time or spare parts for different outcomes.
7. The field-operations board gives the crew two EVA slots per Sol. Players can scrub dusty panels, navigate the rover to collect samples, analyze samples in the lab, or repair an offline communications relay. Failed attempts still use a slot; rover battery recharges slowly.
8. The communications relay affects the Sol 23 warning. Leaving it offline causes an additional simulated late-warning penalty.
9. Cadet XP, levels, skill progress and badges persist locally between runs. The debrief records resources, field jobs and the decisions that shaped the mission.
10. Restarting begins a new run and resets mission resources and one-shot task results; persistent cadet progress remains.
