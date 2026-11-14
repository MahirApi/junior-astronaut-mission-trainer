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


## Mission progression and one-shot setup tasks
- Preserve the training bay → selectable site → visual landing arcade → landing confirmation → crew assignment → four commissioning minigames → 30-Sol campaign. The training bay is not a quiz or assessment.
- Do not add knowledge quizzes, multiple-choice science tests, or scored preflight questions. Skill tiers begin with guided play and progress through XP earned by playing minigames.
- Cadet XP, skill progress and badges may persist locally. Mission resources, incident outcomes and one-shot minigames reset on a new run.
- The player is the captain; four specialists each have a distinct field and are assigned one task apiece.
- A task has one submitted attempt per run. Never add an in-task retry or silently reset a failed result.
- The mission lasts 30 game Sols. A no-change/default allocation run should fail before the end; a thoughtful strategy should be capable of reaching Sol 30.
- A full mission restart may reset all task outcomes, but the debrief must explain failed tasks and their downstream resource consequences.
- Failed commissioning and later crisis events must change simulation state and expose meaningful captain recovery choices. Do not present failure as cosmetic.
- An over-budget plan must have visible, numerical consequences. Raising every allocation to maximum must not outperform a focused strategy.
- Show requested versus delivered allocations in the forecast. Clearly explain when a repair cannot begin because its power threshold or spare-parts cost is unmet.
- The default power preset must not carry the outpost through all 30 Sols without active decisions.
- Power is a shared pool: serve habitat essentials first, then proportionally ration the remaining available energy across player requests. Battery surplus carries forward.
- Daily slider allocations persist until changed by the player; do not silently reset their plan every Sol.
- Each major repair must be selected as a target from its component inspector, meet a minimum delivered-power threshold, and consume one limited spare kit. The mission starts with three kits for four later repairable faults.
- Keep seven major crisis beats on Sols 3, 7, 11, 15, 19, 23 and 27, plus seven choice incidents on Sols 5, 9, 13, 17, 21, 25 and 29. Choice effects must persist and be recorded in the debrief.
- Field operations offer three slots per Sol, including Sol 1. Panel cleaning, rover exploration, sample analysis, signal recovery, cave geology, astronaut rescue, local-resource prospecting, emergency repair and base construction consume a slot; unsuccessful attempts also consume a slot.
- Rover battery recharges slowly. Do not allow unlimited rover trips or unlimited fieldwork in one Sol.
- Cadet skills can tune challenge length and guidance, but must grow through actual play. Never use quiz correctness as a proxy for a student's real-world capability.
- Open the mission alert briefing when a crisis begins and show active faults on the matching outpost hotspot.
- Keep the minigames short, accessible, keyboard/touch friendly, and explain their objective before the one-shot submission.


## PONYTAIL implementation discipline
- Follow the uploaded PONYTAIL "lazy senior dev" guide: inspect the code and all affected paths before changes, reuse the existing single-file patterns, and make the smallest complete change.
- Do not add frameworks, dependencies, speculative options or abstractions. Update every affected caller and document meaningful behavior changes.
- Non-trivial route, energy, parser or simulation logic must include a small self-check. Keep accessibility and safe failure handling.
- End a development update by stating what was not checked and any important risk; never claim a browser playtest unless it happened.

## Play-first minigame rules
- The training bay must not contain a knowledge test. Cadet skill tracks are earned through completed play.
- The landing experience is a live visual arcade with hold-to-control engine and steering inputs, continuously updating speed, crosswind, fuel and pad position. It is not a numeric worksheet or a flight-training tool.
- The sample lab is a tactile scanner sweep. Do not turn scientific interpretation into a multiple-choice exam.

## Long-range rover expedition rules
- Rover excursions must use continuous open-world movement, not a grid or tile-step controls. Include a full outbound and return drive across a procedural visual terrain field.
- Keyboard controls use arrow keys and WASD; on-screen directional controls provide an accessible touch alternative.
- Terrain affects battery cost: uphill is more expensive than level terrain and downhill is cheaper. Sand/rubble may add resistance; boulder/crater impacts and repeated wandering add rover wear.
- Generate a guaranteed traversable route and calculate its round-trip energy plus science-tool costs before enabling the expedition. Never make the designed safe route impossible for the available battery.
- If battery is depleted or wear immobilizes the rover, switch to a guided EVA recovery walk along the path already travelled. Interrupting or aborting an expedition must not silently discard it.
- A rover experiment not returned to base is recorded as failed for that Sol; add 400 metres to the next generated follow-up traverse. The displayed distance is a game-scale unit, not surveyed Mars mileage.
- Rover science can include terrain-camera imagery, wheel odometry/slip observations, environmental sensor readings, panorama, remote chemistry/mineralogy and a sealed/cached sample. Label every observation as simulated game data, never NASA telemetry.


## Commissioning interactions are play, not quizzes
- Solar array: route each live cable by dragging it to its matching bus socket; accessible socket controls are also provided.
- Water recycler: adjust the intake, recirculation pump and filter bypass while watching live pressure and flow gauges.
- Greenhouse: tune water, light and nutrient dials while the seedling responds visually.
- Radiation shelter: drag the sealant brush across exposed seams; the limited supply rewards careful strokes, with a keyboard-accessible patch action.
- Keep feedback inside the activity. Do not ask players to memorize a pattern, choose the correct answer from a list, or submit a multiple-choice assessment.


## NASA-aligned surface-power and upgrade economy
- Model a steady primary fission supply and optional supplemental solar arrays. Solar dust/array damage must not remove the primary fission baseload.
- Current game scale: 1 internal energy unit = 100 kWh; the modeled primary fission baseload is 10 units (1,000 kWh per Sol), with 3 supplemental solar units from the selected extra-solar-wing payload and another 3 from a constructed solar wing. These are classroom game values inspired by NASA architecture material, not a reactor design.
- Battery storage is an energy reserve, not a points wallet. Construction spends stored kWh, available metal/regolith/polymer/electronics inventory and one of the day's operation slots.
- Badge-earned style tokens may purchase cosmetics only. Never let XP, Science Data, badges or style tokens replace electricity or construction materials for engineering upgrades.
- Keep the operations board at three available operation slots per Sol, including Sol 1.
- The game includes landing, day-to-day outpost operations, and a final evacuation sequence. Do not add the floating meteor-shower resupply/point-collection minigame: it does not reinforce the challenge objective.
- Retained optional activities must connect to a mission purpose: cave geology and rover prospecting inform local-resource knowledge; the signal activity supports communications; rescue and final extraction support crew safety; emergency repair and base construction support outpost reliability.
