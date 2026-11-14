# OUTPOST ZERO — Junior Astronaut Mission Trainer

A browser-playable Mars outpost management game for the 2026 NASA Space Apps Challenge.

**Status:** Expanded playable prototype. The game now includes play-earned Cadet skills (no quiz), a live hold-to-control landing arcade, three selectable Mars training sites, four adaptive one-shot commissioning minigames, a 30-Sol campaign, seven major crises plus seven captain-decision incidents, a shared power budget, three repair kits, two field-operation slots per Sol, hands-on panel cleaning, long-range procedural rover expeditions, a drag-to-scan sample lab, relay wiring, cadet XP/levels/badges, and an optional NASA DONKI SEP lookup in `index.html`.

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
1. Cadet skill tracks start with guided challenges and become more demanding through XP earned by actually playing minigames. There is no knowledge quiz or scored preflight test.
2. Choose Gale Crater, Jezero Crater or Utopia Planitia. Each route has a small, clearly described gameplay modifier; these are scenario presets, not claims that a real mission should land at a particular place.
3. Play a live landing arcade. Hold the main engine to slow descent and use arrow keys/WASD or touch thrusters to counter changing crosswinds. Fuel, speed and pad position update continuously. A rough landing causes persistent equipment damage and consumes a spare kit.
4. Assign four specialists to one hands-on operation each: drag live cables into the solar bus, balance water pressure and flow, tune greenhouse water/light/nutrients while watching the seedling respond, and brush sealant across the shelter seams. These are playable control challenges, not quizzes or answer-selection tasks. Each has one attempt per run, and failed outcomes remain in the run.
5. Manage 30 Sols through a shared power budget, persistent allocations and three spare repair kits.
6. Major crisis beats arrive on Sols 3, 7, 11, 15, 19, 23 and 27. Additional captain-decision incidents on Sols 5, 9, 13, 17, 21, 25 and 29 ask the player to trade water, battery, food, crew safety, science time or spare parts for different outcomes.
7. The field-operations board gives the crew two EVA slots per Sol. Players can scrub dusty panels, drive a long procedural rover traverse with arrow keys/WASD (or touch controls), scan returned samples by dragging over a specimen, or repair an offline communications relay. At the destination, four simplified science actions collect a Mastcam-Z panorama, SuperCam chemistry reading, sealed sample core and MEDA-style weather snapshot. The rover must travel out and back; slopes change energy use, hazards damage the rover, and a stranded rover requires a crew walk-back along its tire track. A failed rover experiment is recorded and adds four map tiles to the next Sol's follow-up traverse. All instrument outputs are simulated game data, not NASA telemetry.
8. The communications relay affects the Sol 23 warning. Leaving it offline causes an additional simulated late-warning penalty.
9. Cadet XP, levels, skill progress and badges persist locally between runs. The debrief records resources, field jobs, captain decisions, and the last rover experiment including failures and simulated observation counts.
10. Restarting begins a new run and resets mission resources and one-shot task results; persistent cadet progress remains.
