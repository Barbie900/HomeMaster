# Room type: bathroom (and WC)

Type id: `bathroom`. Wet room. The most complex room per m²: all the trades meet here.

## What makes it different
- Water everywhere: **waterproofing, falls and ventilation** matter more than looks.
- **Electrical safety zones** and IP ratings (electrical.md).
- Small, so mistakes in levels, tile layout and outlet positions show immediately.
- Often the only bathroom: the schedule depends on drying times (screed, CM, waterproofing).

## Decide first
- Shower (walk-in tiled vs. tray) vs. bath, drain type, WC type (wall-hung with frame vs. floor-standing)
- Finished floor level and the floor build-up
- Underfloor heating? Towel rail? Extraction type
- Tile format and layout (aligned to the doors, niches and drain)

## Task sequence (graph ids)
**Work packages:** this room is delivered in **45 small steps** (`packages.yaml` and `sequences.yaml`, the bathroom list). Run `/homemaster:plan-room` for the ordered list and `/homemaster:next-step` for one step at a time. The graph order below is the same sequence at task level.

`survey-and-permits` → `water-heating-plan` → `demolition` → `plumbing-rough-in` → `water-heating-install` → `electrical-rough-in` → `ventilation` → [`underfloor-heating`] → `drywall-wet` and/or `wall-plaster-repair` → `screed` (+ CM test and heating-up protocol) → `waterproofing` → `wall-tiling` → `floor-tiling` → `grouting` → `ceiling-finish` (painted before wall tiling if possible) → `door-install` → `sanitary-fit-out` → `shower-glass-install` → `silicone-joints` → `electrical-fit-out` (+ licensed measurement)

## Room-specific rules and numbers
- Zones 0/1/2, 30 mA RCD, IP ratings: see `trades/electrical.md`.
- Waterproof the **whole floor** and shower walls to ≥ 200 cm. Falls 1.5–2% in shower areas.
- Floor tiles slip rating suitable for wet barefoot areas (ask for the class for barefoot wet areas, e.g. B or C in DIN 51097), and a grout in water-resistant class.
- Extract 60–100 m³/h, with a replacement-air route under the door.
- Hot-water supply close, or a circulation line, to avoid cold-water waiting.
- **WC / toilet room variant:** the same sequence without the shower. Hand basin with a small waterproofed splash zone, frame and cistern in the wall (drywall with backing), extraction required if windowless, door swing outward if the room is tiny.

## Extra interview questions
- Shower type and size, bath wanted, double basin, washing machine here?
- Where is the soil stack? Is the stack accessible and its diameter known?
- Windowless? Ceiling height? Any drop ceiling possible?
- Accessibility needs now or in the future (step-free shower, grab-bar backing)?

## Common mistakes
- Moving the shower after the rough-in.
- Tiling before the CM test and the heating-up protocol.
- Not planning the extract fan and the make-up air.

## Links to other rooms
- Hallway door and threshold height, laundry in the basement or kitchen, tile choices that match the hallway.
- Heating: a towel rail and UFH may need the same manifold as other rooms.
