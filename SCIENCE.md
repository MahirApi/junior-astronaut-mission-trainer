# Science and data traceability

## Purpose
This document separates source observations from the educational model used by OUTPOST ZERO. Game percentages and resource units are teaching abstractions, not engineering design values.

## NASA data integration in the prototype

### NASA DONKI — Solar Energetic Particle (SEP)
- Service: NASA Open APIs, DONKI SEP endpoint.
- API documentation/catalog: https://api.nasa.gov/
- NASA CCMC DONKI: https://ccmc.gsfc.nasa.gov/DONKI/
- Endpoint pattern: `https://api.nasa.gov/DONKI/SEP?startDate=YYYY-MM-DD&endDate=YYYY-MM-DD&api_key=DEMO_KEY`
- The browser app requests a recent 30-day window when the player presses **Load NASA data**.
- The app displays the most recent returned event date and, when supplied, its NASA record link.
- If the request fails or no records are returned, the app continues offline and labels the Sol 23 activity as a simulated training event.

**Interpretation limit:** DONKI SEP records describe space-weather observations/analysis. The prototype does not convert a DONKI event into a Mars-surface radiation dose. A returned record is used as real-world context for the Sol 23 shelter decision exercise, not as measured radiation at Gale Crater.

## Supporting NASA references
- NASA Life Support Baseline Values and Assumptions Document (BVAD): https://ntrs.nasa.gov/citations/20210024855
- NASA, Mars Surface Power Generation Challenges and Considerations: https://www.nasa.gov/wp-content/uploads/2024/01/mars-surface-power-generation-challenges-and-considerations.pdf
- NASA Humans to Mars overview: https://www.nasa.gov/humans-in-space/humans-to-mars/
- NASA/JPL, Martian Dust Devil Whirls Into Opportunity's View: https://www.jpl.nasa.gov/news/martian-dust-devil-whirls-into-opportunitys-view/
- NASA, Growing Plants in Space (Veggie): https://www.nasa.gov/exploration-research-and-technology/growing-plants-in-space/
- NASA Science, Mars Phoenix: https://science.nasa.gov/mission/mars-phoenix/
- NASA, Meteoroid Environment Office overview: https://www.nasa.gov/meteoroid-environment-office/overview/
- NASA, 2023 Space Station water-recovery achievement: https://www.nasa.gov/missions/station/iss-research/nasas-2023-space-station-achievements/
- NASA Science, MOXIE oxygen demonstration: https://science.nasa.gov/resource/the-sound-of-moxie-at-work-on-mars/
- These references support learning themes only: wind can sometimes clean rover solar arrays; plant growth systems need balanced water, nutrients and airflow; Phoenix found subsurface water ice and perchlorate in Martian soil; meteoroid impacts can damage spacecraft; and NASA has demonstrated 98% water recovery on the ISS. The prototype's events and game outcomes are not direct replications of those missions.
- The current playable prototype does not claim its resource percentages or power units are scaled BVAD engineering specifications or a real Mars outpost design.

## Simulation assumptions (game-only)
- The mission lasts 30 game Sols and tracks a fictional five-person crew.
- Cadet skill tracks start in Practice and become more demanding through XP earned by playing the minigames. There is no knowledge quiz or scored preflight assessment; XP is a game progression system, not a measure of student knowledge.
- Habitat essentials draw a fixed four game power units per Sol before the player allocations are served. The remaining supply is a shared pool divided proportionally among requested life-support, greenhouse, shelter and maintenance allocations. Over-budget allocations receive only a fraction of the requested power.
- A successful solar commissioning minigame adds starting battery reserve; solar generation, battery capacity and dust penalties are simplified deterministic rules. NASA's Mars surface power studies consider architectures beyond the solar-only system shown in this game.
- The player carries three abstract spare repair kits. Servicing a major filter, greenhouse, seal or heater fault consumes one kit when a repair successfully begins. This scarcity is a game mechanic, not a NASA supply estimate.
- Major repairs require a selected component target, enough delivered power to meet its start threshold, and sustained allocation across multiple Sols. Allocating power to the wrong system does not repair the fault.
- Life-support allocation affects the oxygen balance and water recovery. A scripted filter clog increases water loss until the player prioritizes Life Support.
- Greenhouse allocation consumes water and advances crop progress. Harvests occur only after a growth threshold, not instantly. A scripted crop blight reduces growth until Greenhouse power is sustained.
- A scripted habitat seal leak drains oxygen until Maintenance is assigned; shelter allocation and a selected passive regolith upgrade affect the one-time simulated crew-safety penalty during the Sol 23 shelter drill.
- Seven major crisis beats occur on Sols 3, 7, 11, 15, 19, 23 and 27. Seven additional incident choices occur on Sols 5, 9, 13, 17, 21, 25 and 29. Timings, effects and choices are designed game mechanics, not a prediction of real Mars weather or equipment failures.
- The live landing arcade, field-operation EVA slots, rover routes, radio-relay repair, sample tasks, Cadet XP and badges are game mechanics. Holding the engine and side thrusters changes the simplified speed/crosswind model; a successful in-game landing does not teach or certify real piloting.
- Selectable site presets adjust fictional starting resources. They are not landing recommendations or real local-resource assessments for Gale, Jezero or Utopia.
- Field science cards use NASA facts as context. For example, wind-cleaning events increased Opportunity solar-array output; NASA's Veggie system balances water, nutrients and airflow; Phoenix found water ice and perchlorate; NASA documents meteoroid impact risks; ISS life support has demonstrated 98% water recovery; and MOXIE produced oxygen on Mars. None of these NASA outcomes are calculated or reproduced by the game's simplified resource model.
- Food and water are consumed over time. Crew safety can decline if reserves become critically low. The all-maximum allocation strategy is intentionally insufficient: power rationing lowers the actual power delivered to every requested system, prevents some repairs from starting, and allows reserves to run down. The player must change priorities and accept that some systems will temporarily receive less.
- The exact power budget, battery reserve, repair thresholds, spare-kit count, EVA capacity, rover battery, landing tolerance, site bonuses, XP rewards and resource rates are invented training values. They are not scaled spacecraft engineering specifications or an operational Mars habitat design.
- The visual landing arcade uses an intentionally simplified speed/crosswind model. It is not a physics-accurate Mars descent simulation and must not be presented as piloting instruction.
- The solar-cable routing, recycler pressure balancing, grow-bed tuning, shelter seam sealant, relay repair, drag-to-scan sample activity and rover science actions are simplified educational interactions, not operational spacecraft, repair, laboratory or rover-command procedures.

## Source eligibility check before submission
The NASA Space Apps Global Awards requirement is to use a NASA data source listed in the **Resources section of this exact challenge**. Before submitting, compare the challenge's live Resources list with the NASA Open APIs / DONKI source above and preserve a screenshot or written record of the match. Do not assume that a generally valid NASA API automatically satisfies the challenge-specific rule.

## Attribution
NASA data and NASA public documentation remain the work of their respective providers. This prototype is an independent educational simulation and is not an official NASA product.


## Crew commissioning minigames (game-only mechanics)
- The fictional five-person crew includes four specialists and the player as captain.
- The captain assigns one distinct specialist to each pre-Sol commissioning task: solar array wiring, water recycler startup, greenhouse calibration, and shelter seam inspection.
- Each minigame resolves once per mission. A wrong submitted action permanently records a failed commissioning outcome for that run. There is no per-task replay.
- A failed solar task reduces modeled solar output; a failed recycler task increases modeled water loss; a failed greenhouse task reduces crop-growth efficiency; and a failed shelter task reduces modeled protection during the scripted shelter drill.
- Correct specialty assignment is shown to the player. An out-of-specialty assignment increases the modeled failure severity; it does not alter any real human or engineering performance data.
- Later captain power allocations can mitigate some simulated consequences. For example, maintenance repairs modeled array damage over multiple Sols, and additional life-support or shelter power can partly compensate for recycler or shelter problems.
- These are designed game rules, not NASA operational procedures, empirically validated crew-performance models, or spacecraft engineering recommendations.


## Rover expedition science analogies (game-only)
The long-range rover activity borrows the *types* of observations made by Mars rovers. It does not reproduce their flight software, instrument calibrations, science data products, drive-planning procedures, or real telemetry.

- **Terrain imaging and navigation:** NASA/JPL describes rover navigation that uses stereo camera imagery to identify steep slopes, rough terrain and large steps; Curiosity also uses visual odometry to compare image features before and after driving and estimate slip. The game uses procedural terrain, simulated Navcam frames, a wheel-move/odometry counter and a simple energy/wear rule. See [JPL Surface System Software and Rover Navigation](https://robotics.jpl.nasa.gov/what-we-do/flight-projects/mars-science-laboratory/surface-system-software-and-rover-navigation/) and [NASA: Curiosity Tracks Its Tracks](https://science.nasa.gov/resource/curiosity-tracks-its-tracks/).
- **Panoramas and geology:** Mastcam-Z on Perseverance captures high-definition colour panoramas and 3D/stereo images; SuperCam uses a camera, laser and spectrometers to investigate rock and soil chemistry/mineralogy. The game presents simplified Mastcam-Z panorama and SuperCam remote chemistry interactions as mini activities. See [NASA Perseverance Science Instruments](https://science.nasa.gov/mission/mars-2020-perseverance/science-instruments/).
- **Environmental conditions:** Perseverance's MEDA instrument measures wind speed and direction, temperature and humidity, and also measures the amount and size of dust particles in the Martian atmosphere. The game offers a MEDA-style sensor snapshot and counts simulated data sets; it does not generate measured Mars weather values. See [NASA Perseverance Science Instruments](https://science.nasa.gov/mission/mars-2020-perseverance/science-instruments/). See [NASA Planetary Data System: MEDA instrument description](https://pds.nasa.gov/ds-view/pds/viewContext.jsp?identifier=urn%3Anasa%3Apds%3Acontext%3Ainstrument%3Amars2020.meda&version=1.3).
- **Sample collection:** Perseverance drills rock cores and seals sample tubes for caching. The game uses a simplified "drill, seal and cache" interaction and only records a returned sample after the rover drives back to base. See [NASA: Perseverance's first sample acquisition](https://www.nasa.gov/news-release/nasa-perseverance-mars-rover-to-acquire-first-sample/).
- **Wheel wear and route choice:** Curiosity has encountered wheel wear and slip on rough or sandy slopes; rover planners have changed routes to avoid damaging terrain. The game's battery percentages, tile costs, slope values, wear meter and collision penalties are invented training rules, not engineering limits. See [NASA/JPL: Curiosity's Navcams View Its Wheels](https://www.jpl.nasa.gov/images/pia26016-curiositys-navcams-view-its-wheels/) and the JPL navigation reference above.
- **Science targets:** Layered sedimentary outcrops, crater walls/ejecta, altered bedrock, soil, and possible ice-related ground are educational prompts inspired by rover geology investigations. The overhang/alcove task is a fictional survey from outside an entrance; the rover does not enter a cave and the game does not claim that NASA rovers explored a Martian cave.

### Game-only rover accounting
A map tile is not a fixed real-world distance. The generated routes, terrain elevations, battery percentages, energy cost multipliers, collision wear, simulated weather sets, image counts and EVA recovery are invented gameplay quantities. Navcam/Mastcam-Z/SuperCam/MEDA labels refer to the kinds of observations being illustrated; the counts and outputs are fictional. A successful expedition means only that the in-game rover returned to its base.


## Commissioning minigame boundaries
The solar-cable routing, water pressure/flow balancing, greenhouse grow-bed controls and shelter seam-sealant activity are simplified tactile learning interactions. Their pressure bands, plant-growth response, sealant supply and commissioning outcomes are invented game mechanics; they are not operational procedures for real spacecraft systems.
