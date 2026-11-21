# Room type: kitchen

Type id: `kitchen`. Semi-wet, high services density: water, drain, gas or 3-phase power, extraction. The layout drawing fixes everything else.

## What makes it different
- **Design before rough-in.** Every service stub must be at the drawn position. Freeze the plan (`kitchen-plan`) first.
- Heavy loads on walls (wall units, extractor), and on the floor (stone worktop, appliances).
- **Extraction and make-up air** and combustion appliances are a safety topic.
- Needs durable, cleanable surfaces: floor, splashback, worktop.

## Decide first
- Layout (I, L, U, island), work triangle, door and window positions, **where the appliances go**
- Cooking energy (induction or electric, or gas), oven type (built-in or freestanding)
- Extraction: duct to the outside (best) or recirculation (carbon filter)
- Floor covering (tile or wood/vinyl), whether it runs under the units
- Worktop material (laminate, solid wood, quartz or stone, ceramic)
- Appliance models (dimensions and connections)

## Task sequence (graph ids)
`kitchen-plan` → `demolition` → `plumbing-rough-in` → `electrical-rough-in` → `ventilation` (extractor duct) → `wall-plaster-repair` → [`screed`] → `wall-finish` → `painting` → `floor-tiling` or `floor-covering-dry` → `kitchen-fit` → `electrical-fit-out` → `sanitary-fit-out` (sink and taps) → `silicone-joints`

## Room-specific rules and numbers
See `trades/kitchen.md` for dimensions (work triangle, heights, clearances), circuits and extraction.
- **Gas:** installation and appliance connection only by a licensed installer. Not DIY.
- **Electrical:** induction hob and oven usually need a dedicated circuit (often 3-phase). Check the panel capacity first (`panel-and-main-services`).
- **Extractor into a shaft:** only if the shaft is meant for kitchens. Never into a bathroom shaft.
- **Open-flue appliances in the same room or in the same ventilation volume** (gas boiler, wood stove): extraction and make-up air need a safety check or interlock by a professional.

## Extra interview questions
- Appliance list with models (fridge, freezer, dishwasher, washing machine, dryer, oven, hob, hood, microwave, steam oven)?
- Gas connection present? Hob type? Which wall for the extractor duct?
- Open to the living room? (Noise, smell, sightlines, flooring continuity)
- Existing positions of the stack, water and drain? Distance sink to stack?
- Who cooks, height of the main user (worktop height)?

## Common mistakes
- Rough-in before the final kitchen drawing, so stubs are off by 10–20 cm.
- Floating floor laid under fixed units.
- No dedicated circuits, or sockets hidden behind appliances where they can't be reached.
- Extractor duct too long or narrow, a "ghost" extractor that does nothing.
- Unsealed worktop cut-outs, swelling.

## Links to other rooms
- Living room (open plan: floor continuity and acoustics), hallway (delivery route), basement (laundry), terrace (door and threshold).
