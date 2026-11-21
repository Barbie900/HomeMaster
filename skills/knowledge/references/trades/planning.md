# Whole-house planning and phases

Graph task: `survey-and-permits`. This file is the order in which a complete renovation is done, and how rooms fit into it. Room-specific sequences are in `references/rooms/<type>.md`.

**DIY level:** the planning is yours. Permits, structural checks and the panel/heat-source connections need professionals in most countries (see the region file).

## Principles of order
1. **Decide house-wide things first, then rooms.** The panel, heat source, ventilation concept, insulation, windows, and the final layout of the kitchen and bathrooms decide what every room needs. Changing them later means opening finished walls.
2. **Structure → weather-tight envelope → services → plaster/screed → drying → finishes → fittings.** **The roof comes first**: interior work under a leaking roof is wasted. Then windows and facade, in that order, so no wall is opened twice.
3. **Dirty before clean, wet before dry, rough before fine, top before bottom.** Chase and plaster before screed, screed before floors, ceilings before walls before floors, floors before kitchen units and furniture.
4. **Do rough-in for the whole house (or a whole floor) in one pass** (electrical, plumbing, heating, ventilation). It is cheaper, and you only photograph and test once.
5. **Drying and curing time is part of the plan.** Use waiting times for the next room's preparation, orders and outdoor work.
6. **Photograph and log everything** with a tape measure. The log drives the dependency checks.

## Phases (graph ids in brackets)
| Phase | What | Notes |
|---|---|---|
| 0 | Survey, permits, budget, hazard survey, priority order (`survey-and-permits`) | the cheap phase that avoids the expensive mistakes |
| 1 | House-wide decisions: panel and load list (`panel-and-main-services`), heat source and emitters (`heating-distribution`), insulation concept (`insulation`), ventilation concept, smart-home standard and cabling plan (`smart-home-plan`), kitchen/bath/wellness layouts (`kitchen-plan`, `wellness-plan`) | most are on paper. Order long-lead items now |
| 2 | Moisture and envelope: **roof first** (`roof-assessment`, `roof-repair`), gutters, ground drainage, basement diagnosis (`site-drainage`, `basement-diagnosis`, `basement-waterproofing`), windows (`windows-install`), insulation, facade (`facade-preparation`, `facade-etics`, `facade-render`), attic conversion (`attic-conversion`), chimney inspection (`chimney-assessment`) | basements need a season to prove they are dry, so start early |
| 3 | Strip-out and structural changes (`demolition`, `partitions-and-ceilings`) | one pass, with dust control |
| 4 | Rough-in: electrical, plumbing, heating, ventilation, **network and smart-home cabling** (`smart-home-cabling`), sleeves under future paving | pressure tests and photographs before closing |
| 5 | Wall repairs, plaster, screed (`wall-plaster-repair`, `screed`, `underfloor-heating`) | long drying. CM tests where tiles or wood follow |
| 6 | Waterproofing and wet-room tiling (`waterproofing`, `wall-tiling`, `floor-tiling`) | after CM and heating-up protocols |
| 7 | Skim, ceilings, painting (`wall-finish`, `painting`), stove and flue connection (`chimney-work`, signed off before first fire) | before dry floors |
| 8 | Dry floors, doors, skirting (`floor-covering-dry`, `door-install`, `skirting-and-trim`, `indoor-stairs-inspection`, `indoor-stairs-work`) | last dusty step done |
| 9 | Fit-out: kitchen, sanitary, fixtures, appliances (`kitchen-fit`, `sanitary-fit-out`, `electrical-fit-out`), smart-home devices and security (`smart-home-commission`) | licensed measurements and sign-offs |
| 10 | Outdoor surfaces and stairs (`outdoor-substrate`, `outdoor-tiling`, `stairs-structure`, `handrail`, `garden-structure-build`, `pool-structure`, `pool-technical`, `pool-heating-and-cover`, `garden-design-plan`, `garden-groundwork`, `irrigation-plan`, `irrigation-install`, `garden-planting`, `pool-season-care`) | in the dry, frost-free season, after heavy deliveries |
| 11 | Wellness (`sauna-build`, `steam-room-build`) | needs the final power and ventilation capacity |

## Choosing the order of rooms
- **Rooms with long drying or lead times first** (bathroom screed, kitchen order). They gate your schedule.
- **Keep one good room.** Don't start with the only bathroom or the only bedroom unless there's a second option for the weeks of works.
- **The hallway is your materials route.** Do it last, and protect its floor with boards and film until then.
- **Basement diagnosis and ground drainage first**, even if the basement is the last room you finish.
- **Outdoor works in season** (typically April–October in central Europe), after trucks and skips no longer need the garden.
- **Do the whole-house rough-in before finishing any room.** Otherwise you'll open finished walls for the next room's cables and pipes.

## Living in the home
- Plan **zones**: sealed dust barriers (zip doors and film), a clean route out, a tool room.
- **Shutdowns:** water and power off for hours or days. Plan a second toilet/shower and a camping kitchen.
- **Noise:** check house rules and neighbours (apartment blocks), tell them the dates.
- **Waste:** ≈ 1–1.5 t per bathroom strip-out, more for screeds and plaster. Order containers and parking.
- **Insurance:** tell your home insurer about the renovation. Check cover for water damage and for work you do yourself.

## Budget and lead times
- Contingency **15–20%** (hidden defects are normal in old buildings).
- Lead times: custom or imported tiles 2–6 weeks, windows 4–10 weeks, kitchens 6–12 weeks, stone and quartz worktops 1–3 weeks after templating, sanitary frames 1–3 weeks.
- **Order after measuring on site** (windows, worktops, kitchen). Keep delivery windows in the plan, with storage space.

## Documentation
- Keep: photo log with the tape measure, the pipe and cable drawings, test reports (pressure tests, CM measurement, electrical measurements), product data sheets and receipts.
- These go into the house's folder for the next owner and for warranty or insurance claims.

## Tips & tricks
- Colour-code the dependency graph on a wall chart: it is the best motivation to stop cutting corners.
- One Saturday a month for **cleaning, tidying and inventory** saves more time than it costs.
- Re-plan after every delay: ask the `project-lead` agent for the new earliest dates.

## Common mistakes
- Starting with the finishes (pretty rooms) and leaving the rough-in for later.
- Ordering windows or kitchens from drawings before measuring on site.
- Not leaving drying time between wet trades and floors.
- No contingency.
- Sanding dust spreading into finished rooms.

## Cross-trade
- Every task in the graph has its `requires`. This file only gives the order. The dependency checker verifies the details per task.
