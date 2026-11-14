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
- These references support the general learning themes: power, life support, shelter, temperature and other systems are coupled; dust storms can reduce solar power for extended periods; and human Mars power architecture is more complex than the prototype's solar-only game model.
- The current playable prototype does not claim its resource percentages or power units are scaled BVAD engineering specifications or a real Mars outpost design.

## Simulation assumptions (game-only)
- The mission lasts 30 game Sols and tracks a fictional five-person crew.
- Habitat baseline demand is four game power units per Sol; player allocations are additional game power units. A simulated heater fault adds demand until Maintenance repairs it.
- Solar generation, battery capacity, dust loss, maintenance recovery and crop growth are simplified deterministic rules. NASA's Mars surface power studies consider architectures beyond the solar-only system shown in this game.
- Life-support allocation affects the oxygen balance and water recovery. A scripted filter clog increases water loss until the player prioritizes Life Support.
- Greenhouse allocation consumes water and advances crop progress. Harvests occur only after a growth threshold, not instantly. A scripted crop blight reduces growth until Greenhouse power is sustained.
- A scripted habitat seal leak drains oxygen until Maintenance is assigned; shelter allocation and a selected passive regolith upgrade affect the one-time simulated crew-safety penalty during the Sol 23 shelter drill.
- The seven crisis beats occur on Sols 3, 7, 11, 15, 19, 23 and 27. Their timing and effects are designed game mechanics, not a prediction of real Mars weather or equipment failures.
- Food and water are consumed over time. Crew safety can decline if reserves become critically low. The baseline/default plan is intentionally insufficient for the full 30-Sol campaign; players must make changing priorities and accept that some systems will temporarily receive less.

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
