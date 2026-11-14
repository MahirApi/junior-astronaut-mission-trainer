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
- If the request fails or no records are returned, the app continues offline and labels the Sol 4 activity as a simulated training event.

**Interpretation limit:** DONKI SEP records describe space-weather observations/analysis. The prototype does not convert a DONKI event into a Mars-surface radiation dose. A returned record is used as real-world context for a shelter decision exercise, not as measured radiation at Gale Crater.

## Supporting NASA life-support reference
- NASA Life Support Baseline Values and Assumptions Document (BVAD): https://ntrs.nasa.gov/citations/20210024855
- Use BVAD for background research and to explain that oxygen, water, food, and power budgets are coupled.
- The current playable prototype does not claim its resource percentages or power units are scaled BVAD engineering specifications.

## Simulation assumptions (game-only)
- The mission lasts seven game Sols and tracks an abstract three-person crew.
- Habitat baseline demand is four game power units per Sol; player allocations are additional game power units.
- Solar generation, battery capacity, dust loss, maintenance recovery and crop growth are simplified deterministic rules.
- Life-support allocation affects the oxygen balance and water recovery.
- Greenhouse allocation consumes water and advances crop progress. Harvests occur only after a growth threshold, not instantly.
- Shelter allocation and a selected passive regolith upgrade affect the crew-safety penalty in a scripted training scenario.
- Food and water are consumed over time. Crew safety can decline if reserves become critically low.

## Source eligibility check before submission
The NASA Space Apps Global Awards requirement is to use a NASA data source listed in the **Resources section of this exact challenge**. Before submitting, compare the challenge's live Resources list with the NASA Open APIs / DONKI source above and preserve a screenshot or written record of the match. Do not assume that a generally valid NASA API automatically satisfies the challenge-specific rule.

## Attribution
NASA data and NASA public documentation remain the work of their respective providers. This prototype is an independent educational simulation and is not an official NASA product.
