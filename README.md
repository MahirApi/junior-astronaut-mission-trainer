# OUTPOST ZERO — Junior Astronaut Mission Trainer

A browser-playable Mars outpost management game for the 2026 NASA Space Apps Challenge.

**Status:** Expanded playable prototype. The mission arcade uses the supplied JuniorAstronaut reference implementations for precision landing, cave exploration, three-room emergency repair, tethered orbital rescue, signal recovery, drill-heat resource prospecting and the three-stage finale. The reference's synthesized music, canvas effects, remappable controls/settings and two-player shared-keyboard station game are included too. OUTPOST ZERO keeps its 30-Sol campaign, fission-primary/solar-auxiliary power, energy-and-material-based construction economy, four hands-on commissioning activities, three daily operation slots, large continuous open-world rover and cosmetic-only rewards. The floating meteor-supply pickup activity remains intentionally excluded.

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
NASA DONKI provides real space-weather records. The game uses a returned SEP record as context for a simulated Sol 23 shelter drill; it does **not** turn that record into a Mars radiation dose. NASA selected nuclear fission as the primary surface-power technology for initial crewed Mars missions in its 2024 architecture review. OUTPOST ZERO reflects that architectural direction with a constant modeled fission baseload and dust-sensitive solar support. Its energy units are simplified teaching values, not an engineering design. Dust, filter, crop, pressure-seal, storm and heater incidents are authored scenarios, not NASA forecasts. Check `SCIENCE.md` and verify the exact challenge Resources list before submission.

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
4. Commission the core systems through four hands-on operations available on the daily board: drag live cables into the solar bus, balance water pressure and flow, tune greenhouse water/light/nutrients while watching the seedling respond, and brush sealant across the shelter seams. These are playable control challenges, not quizzes. Each has one attempt per run, and failed outcomes remain in the run.
5. Manage 30 Sols through a shared power budget, persistent allocations and three spare repair kits.
6. Major crisis beats arrive on Sols 3, 7, 11, 15, 19, 23 and 27. Additional captain-decision incidents on Sols 5, 9, 13, 17, 21, 25 and 29 ask the player to trade water, battery, food, crew safety, science time or spare parts for different outcomes.
7. The daily operations board gives the crew three operation slots per Sol. Activities include solar-panel cleaning, a continuous open-world rover expedition, lab sample scanning, communications recovery, oxygen-limited cave geology, the reference-style three-room emergency repair, reference-style tethered orbital rescue, Mars ISRU drilling with reference drill-heat physics, and construction of new outpost modules. The rover uses keyboard/touch drive controls, procedural terrain, slopes, rocks and craters; the crew must collect three samples and return to base. A stranded rover triggers an EVA walk-back and a longer follow-up traverse. Camera, wheel-odometry, chemistry, sample and weather records are simulated game observations, not NASA telemetry.
8. The communications relay affects the Sol 23 warning. Leaving it offline causes an additional simulated late-warning penalty.
9. After Sol 30, the reference-style three-stage evacuation runs as one continuous mission: restore the power lines, recover the crew and launch through the debris field. Base construction spends stored electricity (shown in kWh), a stock of construction materials and one daily operation slot. Badge-earned style tokens buy suit/rover cosmetics only; they cannot purchase life-support capacity, repairs, power or survival upgrades. Cadet XP, levels, skills, badges and cosmetic unlocks persist locally. The debrief records resources, field jobs, captain decisions and rover results.
10. Restarting begins a new run and resets mission resources and one-shot task results; persistent cadet progress remains.


## Power and construction
The game expresses stored and generated energy in kWh (one internal energy unit represents 100 kWh). Its power mix uses a steady 1,000 kWh/Sol modeled fission baseload plus supplemental solar generation from the selected payload and any constructed solar wing. Dust and array damage reduce only the solar contribution. This is a teaching abstraction inspired by NASA's fission-primary Mars surface-power architecture, not a specification for a real reactor or habitat. Module construction consumes stored kWh, construction materials and one operation slot. Cadet style tokens are cosmetic-only.


## Reference minigame parity
The team-provided `JuniorAstronaut.html` is the implementation reference for the mission arcade. Landing, cave, repair, rescue, signal, prospecting and finale use the reference canvas factories for visuals, movement, timing, interactions, hazards and success/failure rules. An OUTPOST ZERO adapter routes the results into this project's campaign rather than importing the reference's older 14-Sol / tech-points simulation. The mining activity is re-themed as Mars local-resource prospecting / ISRU; its drill heat-management physics are kept. The compact reference rover is not used: OUTPOST ZERO keeps its larger continuous procedural rover expedition. The floating meteor-supply pickup game remains excluded, while debris hazards in the final evacuation remain part of the finale.
