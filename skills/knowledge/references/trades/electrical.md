# Trade: Electrical (bathroom)

Graph tasks: `electrical-rough-in`, `electrical-fit-out`. **Rules differ by country**: always read `regions/<cc>.md`.

**DIY level:** the homeowner can usually do **planning, chasing, laying conduits and boxes, and preparation**. **Not DIY** in most of Europe: connecting to the distribution board, new circuits, equipotential bonding, and the **inspection and measurement/certification** (needed before use and for insurance). Ask a licensed electrician to do the connections and to measure. Agree on what you prepare before they come.

## Concepts you must know
- **Zones** (IEC 60364-7-701; dimensions vary slightly with the version your country uses, so ask a licensed electrician or check the local standard):
  - **Zone 0:** inside the bath or shower tray. IPX7.
  - **Zone 1:** above zone 0 up to ≈ 225 cm (for a walk-in shower: around the fixed shower head). IPX4 minimum; **no sockets or switches**.
  - **Zone 2:** ≈ 60 cm around zone 1. IPX4 minimum; no sockets.
  - **Outside the zones:** IP20 minimum if splashing is excluded, but keep sockets ≥ 60 cm from a bath/shower edge in practice.
- **RCD (FID) 30 mA** protects all bathroom circuits (including lights).
- **Supplementary equipotential bonding** of metal pipes and conductive parts where the local rules require it.
- **Circuit separation:** separate circuits for lights, sockets, a heated towel rail, underfloor heating and the washing machine. Check that the main board has free modules before you plan the circuits.

## Planning checklist
1. Mark FFL line and fixture positions, zones, the shower position and the door swing.
2. List all electrical items: ceiling light(s), mirror light, extract fan (timer or humidity sensor), shaver socket, a socket for hair dryer outside zone 2, towel rail, UFH thermostat and floor sensor, washing machine, intercom?
3. Typical heights above the FFL: switches ≈ 105 cm, sockets ≈ 30 cm (or ≈ 105 cm by the basin, outside zone 2). Use the same heights as the rest of the home.
4. **Run conduits for everything now**, including the future items (towel rail, second light).
5. Cable sizes (typical; the electrician decides): lights 3 × 1.5 mm², sockets 3 × 2.5 mm², fan 3 × 1.5 mm², UFH thermostat per its power, towel rail per its power. Use conduit for later replacements.

## Materials
- Corrugated conduit (flexible) or rigid; wall boxes deep enough (60 mm for switches with a thermostat)
- NYM-J (or the cable type your country prescribes)
- Cable clips, dustproof boxes, labelling tape
- Plaster-proof boxes and sealing tape for boxes in wet walls
- UFH: sensor conduit with a bend radius ≥ 5× diameter, into the floor to the middle of two pipes

## Tools
- Voltage tester, circuit tracer, multimeter (have/buy)
- Wall chaser + M-class extractor (rent), SDS-plus drill with a core bit for boxes
- Pull-wire/fish tape, conduit bender (springs), cable cutter and strippers

## Method: DIY preparation
1. **Dead:** switch off, verify at the exact boxes, tag the breaker. Never trust labels on the board.
2. **Chase routes** (see demolition): horizontal and vertical only, in the preferred zones: horizontal ≈ 30 cm below the ceiling or 30 cm above the floor; vertical 10–20 cm from corners and door frames. Not diagonal. Avoid running near water pipes.
3. **Boxes:** core-drill, set with plaster, align to the wall surface plus the planned tile thickness (**boxes must be flush with the *finished* wall**: wall + adhesive + tile).
4. **Conduits** with gentle bends, leaving pull wires. Seal conduit ends against moisture and plaster.
5. **Cables** are pulled by the electrician, or by you if you agree. Leave 20–30 cm of slack in every box.
6. **Photograph everything** with a tape measure and keep a drawing of the routes.

## Fit-out (finishing, by the electrician)
- Fixtures must carry the **IP rating for their zone** (see above). LED drivers belong outside zone 1, or in IP-rated housings.
- Extract fan wired to light switch with a run-on timer (15–20 min) or humidity sensor.
- UFH thermostat: sensor in conduit, floor limit sensor (max floor temp, typically 29 °C living areas, up to 33 °C bathrooms).
- Measurements and the report (insulation resistance, RCD trip time, loop impedance, continuity of protective conductor) → the **inspection report** you keep with the home papers.

## Tips & tricks
- A cheap "snake" conduit trick: pull a string through the conduit on the first run, with the pull cord left in.
- Put a few spare boxes (blanking plates) behind where mirror lights/cabinets can go.
- Test the RCD with the test button after the electrician finishes.

## Common mistakes
- Sockets or switches inside zones 0–2.
- A box not flush with the tiled surface.
- Using the old light fitting without checking its IP rating.
- Forgetting the extract fan wiring: cabling afterwards means chasing the finished wall.
- Skipping the measurement/inspection before use.

## Cross-trade
- Plaster repair must wait for the electrical rough-in photographs.
- UFH thermostat sensor needs the conduit in the **screed**, set before it's poured.
- Tile layout: boxes should land on tile centres or joints. Plan with your tile format.

## Other rooms (whole-house electrical planning)
Same DIY limit as above: you plan, chase, lay conduits and boxes. The licensed electrician connects, certifies and measures.
- **Plan the whole house once** (`panel-and-main-services`): load list, free panel modules, RCDs, earthing, a surge protection and spare circuits. Photograph the panel before work.
- **Circuits per room (typical, check local rules):** lights and sockets on separate circuits, a separate circuit for each large load (oven/hob, dishwasher, washing machine, dryer, heat pump, sauna, EV charger, workshop). Don't put a whole floor on one breaker.
- **Sockets (typical planning guide):** living room 8–12, bedroom 6–8, kitchen 6–10 worktop sockets plus the appliance outlets, hallway 2–3, home office 6–8. More is cheaper before plaster than after. Add **data (network) outlets**, TV/antenna, and a conduit to the roof or garden if needed.
- **Lights:** plan the circuits for ceiling and wall lights, switch positions at the door side (2-way and 3-way switches for long rooms and stairs), dimmers and presence sensors in halls, bathrooms and stairs.
- **Smoke detectors:** in hallways and sleeping rooms, interconnected where required (EN 14604).
- **Outdoor and wet areas:** outdoor-rated cable (UV, buried depth per rules), IP-rated fittings, an RCD, and a separate outdoor isolator. Cellar and utility circuits with RCD, sockets above the flood level.
- **High loads and heat:** sauna heater, steam generator and hot tub are licensed work (`trades/wellness.md`). An EV charger, a heat pump and induction cooking mean checking the connection capacity first.
- **Future-proofing:** spare conduits (Ø25–32 mm) between the panel and the attic/cellar, to the garage and the terrace.
- **Test and document:** the electrician's measurement report for each circuit. Keep the cable drawings.
- **Smart home and low-voltage:** pull network cables, a neutral at every switch box and spare conduits **in the same rough-in pass** (see `trades/smart-home.md`). Keep low-voltage cables ≥ 5–10 cm away from mains cables or in separate conduits.

## Element: sockets and switches (dry rooms)
**DIY limit:** you plan, chase, lay conduit and set boxes. **Connection, the panel and measurements** are the licensed electrician's.
1. **Plan with furniture:** draw the furniture and mark **each socket** at its height (typical ≈ 30 cm above the floor, ≈ 105–115 cm above a worktop or desk, ≈ 105 cm for switches). **Typical counts:** living room 8–12, bedroom 6–8, hallway 2–3, home office 6–8. **More is cheaper now.**
2. **Circuits:** lights and sockets on **separate circuits**, large loads on their own. **Don't put a whole floor on one breaker.** Check the **free modules** in the panel.
3. **Boxes:** **deep boxes (≥ 60 mm)**, **flush with the finished wall** (plaster and paint), **levelled** with a spirit level across multiple boxes, standard spacing for multi-gang frames.
4. **Switches:** next to the door on the handle side, **two-way switches** for rooms with two doors and for stairs, **a neutral in every box**.
5. **Conduits:** continuous from box to box with a **pull wire**, **no more than 270° of bends** between boxes, **gentle radii**. **Label** them.
6. **Photograph** the layout with a tape measure before plastering.

## Element: lighting
1. **Light levels (typical):** living room ≈ 100–150 lm/m² with scenes, kitchen worktop ≈ 300–500 lux, bathroom ≈ 200–300 lux, study ≈ 500 lux, hallway ≈ 100 lm/m², bedroom ≈ 50–100 lm/m² plus bedside lights.
2. **Layers:** general (ceiling), task (desk, worktop, mirror), accent (walls, shelves). **Several circuits** let you dim and mix.
3. **Colour:** about **2700–3000 K** in living spaces, **3500–4000 K** in kitchens and work areas, **CRI ≥ 80–90**.
4. **Recessed spots:** the **ceiling void** (≥ 8–10 cm), **fire-rated or airtight hoods** in insulated ceilings and under the roof (**no plain spots in an airtight layer**). **LED drivers** accessible and ventilated. **Dimmable** lamps matched to the dimmer.
5. **Switch positions** at each door, **dimmers** where wanted, **presence sensors** in halls, bathrooms and stairs.
6. **Rough-in:** a cable to every **ceiling point**, with 20–30 cm of slack in the box. **Fit the fixtures last** (after painting), by the electrician.

## Element: smoke and CO alarms
1. **Smoke alarms (EN 14604):** **in every sleeping room**, **in hallways and escape routes**, **one on each floor** and on the **landing of a stair**. On the ceiling, **≥ 50 cm from walls and lights**, not in kitchens or bathrooms.
2. **Interconnected** (wireless or wired) so one alarm sounds them all. **10-year sealed battery** models are easy.
3. **CO alarms (EN 50291)** near **fuel-burning appliances** and in **sleeping areas next to them**.
4. **Test** monthly. **Replace** by the date on the label. **Never paint over them.**

## Element: TV and media wall
1. **Choose the height** before the wall is closed: **screen centre ≈ 100–120 cm** above the floor (seated eye level).
2. **Backing:** a plywood or steel plate behind the board for a **wall bracket**, rated for the TV's weight with a safety factor of **≥ 2**. **Never** hang a TV on plain plasterboard.
3. **Cables:** **a recessed box (power and data) behind the screen**, and **a separate conduit for HDMI and speaker cables**. **Mains and low-voltage separated** by ≥ 5–10 cm or in different conduits.
4. **Ventilation:** a gap or vents for any **built-in cabinet** with a receiver, **no heat trap**.
5. **Photograph** the positions.

## Element: distribution board work (licensed)
1. **By the electrician only:** adding circuits, RCDs and breakers, **earthing and bonding**, **surge protection**, and **measurements** with the **report**.
2. **You prepare:** the **load list**, the **circuit plan** (room by room), **labels**, **clear access** (≥ 80 cm in front, nothing hung in the way), and **photographs** of the panel before and after.
3. **Keep** the measurement report with the house papers.
