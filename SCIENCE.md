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
- The quiz gives each skill a Practice, Standard or Advanced tier. Correct answers and completed minigames contribute local XP/skill progression. This personalizes gameplay difficulty and is not a validated measure of student knowledge.
- Habitat essentials draw a fixed four game power units per Sol before the player allocations are served. The remaining supply is a shared pool divided proportionally among requested life-support, greenhouse, shelter and maintenance allocations. Over-budget allocations receive only a fraction of the requested power.
- A successful solar commissioning minigame adds starting battery reserve; solar generation, battery capacity and dust penalties are simplified deterministic rules. NASA's Mars surface power studies consider architectures beyond the solar-only system shown in this game.
- The player carries three abstract spare repair kits. Servicing a major filter, greenhouse, seal or heater fault consumes one kit when a repair successfully begins. This scarcity is a game mechanic, not a NASA supply estimate.
- Major repairs require a selected component target, enough delivered power to meet its start threshold, and sustained allocation across multiple Sols. Allocating power to the wrong system does not repair the fault.
- Life-support allocation affects the oxygen balance and water recovery. A scripted filter clog increases water loss until the player prioritizes Life Support.
- Greenhouse allocation consumes water and advances crop progress. Harvests occur only after a growth threshold, not instantly. A scripted crop blight reduces growth until Greenhouse power is sustained.
- A scripted habitat seal leak drains oxygen until Maintenance is assigned; shelter allocation and a selected passive regolith upgrade affect the one-time simulated crew-safety penalty during the Sol 23 shelter drill.
- Seven major crisis beats occur on Sols 3, 7, 11, 15, 19, 23 and 27. Seven additional incident choices occur on Sols 5, 9, 13, 17, 21, 25 and 29. Timings, effects and choices are designed game mechanics, not a prediction of real Mars weather or equipment failures.
- The landing simulator, field-operation EVA slots, rover routes, radio-relay repair, sample tasks, cadet XP and badges are game mechanics. A successful in-game landing does not teach or certify real piloting; the controls are an abstract learning exercise.
- Selectable site presets adjust fictional starting resources. They are not landing recommendations or real local-resource assessments for Gale, Jezero or Utopia.
- Field science cards use NASA facts as context. For example, wind-cleaning events increased Opportunity solar-array output; NASA's Veggie system balances water, nutrients and airflow; Phoenix found water ice and perchlorate; NASA documents meteoroid impact risks; ISS life support has demonstrated 98% water recovery; and MOXIE produced oxygen on Mars. None of these NASA outcomes are calculated or reproduced by the game's simplified resource model.
- Food and water are consumed over time. Crew safety can decline if reserves become critically low. The all-maximum allocation strategy is intentionally insufficient: power rationing lowers the actual power delivered to every requested system, prevents some repairs from starting, and allows reserves to run down. The player must change priorities and accept that some systems will temporarily receive less.
- The exact power budget, battery reserve, repair thresholds, spare-kit count, EVA capacity, rover battery, landing tolerance, site bonuses, XP rewards and resource rates are invented training values. They are not scaled spacecraft engineering specifications or an operational Mars habitat design.
- The manual landing minigame uses an intentionally simplified speed/crosswind model. It is not a physics-accurate Mars descent simulation and must not be presented as piloting instruction.
- The relay and sample-analysis games are simplified classroom puzzles, not operational repair or scientific laboratory procedures.

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
