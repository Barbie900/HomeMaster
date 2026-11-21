# Room type: chimney, stove and fireplace

Type id: `chimney`. A flue and the appliance connected to it: wood stove, fireplace, pellet stove, tiled stove, boiler.

## What makes it different
- **Safety-critical:** carbon monoxide, chimney fire and house fire.
- **Licensed sign-off:** a chimney sweep or installer inspects and approves the flue and the connection before first use.
- **Air:** the appliance and the house compete for air (airtight windows, extractors, ventilation units).
- **Fuel and operating habits** (dry wood, ash handling) decide how safe and clean it is.

## Decide first
- Which appliance (closed wood stove, pellet, tiled stove, open fire, boiler) and which output (kW)
- Existing chimney: liner, height, state, other appliances on it, the sweep's report
- Combustion air (external air connection), kitchen extractor and ventilation conflicts
- Hearth, wall protection and clearances, and where the wood is stored
- Who does the installation and sign-off

## Task sequence (graph ids)
`survey-and-permits` → `chimney-assessment` → [`roof-assessment`] (chimney head and flashing) → `chimney-work` → [`wall-finish` → `painting`] (after the flue and hearth are approved)

## Room-specific rules and numbers
See `trades/chimney.md`.
- Stove output typically 4–8 kW for 40–100 m² of a well-insulated space. Oversized stoves overheat.
- Draught typically ≈ 10–20 Pa, measured by the sweep.
- Hearth typically ≈ 50 cm in front and ≈ 30 cm to the sides (check the maker and the rules).
- A CO alarm (EN 50291) in the room and the sleeping areas, tested monthly.
- Burn dry wood (moisture under ≈ 20%).

## Extra interview questions
- Is there a chimney? Type, liner, age, height, any previous reports from the sweep?
- Which appliance is planned or already in place? Output? Is the home airtight (new windows, ventilation unit, extractor)?
- Hood or ventilation with a fan in the same room or open plan?
- Floor material under the stove, and walls behind it (combustible?)
- Wood storage and delivery route?

## Common mistakes
- Firing an old chimney without a sweep's check.
- No external air in an airtight house, an extractor fighting the stove.
- Too little clearance, no proper hearth.
- Wet wood, rubbish, ignoring the CO alarm.

## Links to other rooms
- Living room (stove), kitchen (extractor), roof (chimney head, flashing), basement or utility room (boiler), facade.
