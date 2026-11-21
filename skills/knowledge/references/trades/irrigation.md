# Trade: Garden irrigation

Graph tasks: `irrigation-plan`, `irrigation-install`. Typical values: the **component makers' instructions**, your **water utility's rules** and the local **well and water-use rules** win.

**DIY level:** a good DIY project (pipes, sprinklers and drip lines are simple). **Licensed:** the **mains connection of the controller or pump** (mains voltage) and **well or borehole work** (permit). **Backflow prevention is required** in many countries so that garden water can't flow back into the drinking supply.

## Decide first
- **Water source:** mains (a tap or a dedicated connection with its own meter), **a well or borehole** (permit and water quality), **a rainwater tank** (best for beds, with a pump and overflow). **Don't use grey water on edible crops.**
- **What to water:** lawn, beds, shrubs, hedges, pots, a vegetable garden. **Drip lines** are the most efficient for beds, trees and hedges, **rotor or spray heads** for lawns.
- **How:** a **hose and timer** (cheapest), **a drip kit**, or **a buried system with zones, valves and a controller**.
- **Control:** a timer with a **rain sensor**, a **smart controller** (weather-based, see `smart-home.md`), and optionally **soil moisture sensors**.

## Measure first (this is the plan)
1. **Flow:** time how long a bucket of known size (10 l) takes to fill from the tap or pump. **Flow (l/min) = bucket litres ÷ minutes.** For example 10 l in 30 s = 20 l/min. **Typical household taps give ≈ 15–30 l/min.**
2. **Pressure:** a gauge on the tap (typically 2–5 bar). **Drip** needs ≈ 1–1.5 bar after a regulator, **sprinklers** typically ≈ 2–4 bar (per the head).
3. **Zones:** each zone's total demand must stay **≈ 70–80% or less of the flow**. Example: 20 l/min available → zone ≤ 14–16 l/min.
4. **Plant water needs:** a lawn typically needs about **25 mm of water per week in summer** (≈ 25 l/m² per week), beds ≈ 15–25 l/m² per week, **trees and hedges** a long, deep soak weekly in dry spells, **newly planted ones more**. Adjust to soil (sand dries fast, clay holds water) and the weather.
5. **Run time = water needed ÷ precipitation rate.** Sprays ≈ 40–50 mm/h, rotors ≈ 10–15 mm/h, drip is quoted in litres per hour per emitter (typically 2–4 l/h).

## Components (typical)
| Part | Notes |
|---|---|
| **Backflow preventer / non-return valve** | at the tap or the manifold, **required by the water utility** in many countries |
| **Filter** (120–150 mesh for drip) and **pressure regulator** (≈ 1–1.5 bar for drip) | the filter is the key to clog-free drip |
| **Main line** (PE pipe 25–32 mm) | buried, with a **shut-off valve** and **a drain point at the lowest spot** |
| **Valves and valve boxes** (24 V AC solenoid valves) | one valve per zone, boxes accessible with gravel below |
| **Controller** | indoor or weather-proof, a rain sensor, 24 V transformer (**mains side by a licensed electrician**) |
| **Lateral pipes** (PE 16–25 mm) and **sprinklers** | **head-to-head spacing** (the spray reaches the next head), matched precipitation within a zone |
| **Drip** (16 mm tube with emitters or a line with drippers) | pegged or buried under the mulch, flush end caps |
| **Sleeves** (Ø50–110 mm) | **under paving and drives, laid before surfacing** |

## Method (task: `irrigation-install`)
1. **Draw the plan to scale** (sources, zones, valve box, pipe routes, heads) and **mark the pipes on the ground** with spray paint. **Locate utilities first.**
2. **Lay sleeves** under paving before it is built (a spare sleeve for power and data too).
3. **Trench:** typically **25–40 cm deep** (below the cultivation depth, deeper for mains in frost areas), **slope the lines to the drain points**. Use a trencher or a spade.
4. **Connect:** the backflow preventer, filter and regulator at the supply, the main to the **valve manifold**, the laterals from each valve. **PE compression fittings** are easy for DIY (cut square, insert fully, tighten), or glued PVC.
5. **Flush every line** before fitting sprinklers or drippers (dirt kills heads).
6. **Fit heads** at the right height (flush with the lawn), adjust the arc and the radius.
7. **Wire** the valves to the controller (24 V cable, one common wire plus one per valve, **a spare pair or two**), with waterproof connectors, and **test each zone by hand**.
8. **Program** the controller (a few long soaks beat frequent shallow ones, early morning), **add the rain sensor**.
9. **Backfill** in layers, **mark the plan** (drawing and photos), and keep the leftovers.

## Winterising (frost areas)
- **Shut the water off** and **drain the lines**: open the drain valves at the low points and **blow out the zones with a compressor** (low pressure ≈ 2–3 bar, **never more than the pipe allows**, and **wear eye protection**). Remove or protect the backflow preventer and the controller. **Frost destroys a system that was not drained.**
- **Re-start** in spring: close the drains, slowly fill, check for leaks, re-set the controller.

## Rainwater and wells
- **Rain tank:** gutter filter, first-flush diverter if needed, **a covered tank**, an **overflow to a soakaway or a drain**, and a pump with a pressure switch. **No cross-connection** with the drinking water supply (a **separate tap or a physical air gap**).
- **Well water:** check the **iron and lime content** (they clog drippers), **filter**, and the **permit and water-use rules**.

## Costs and water rules
- **Metering:** some utilities bill sewage by the metered water. **A separate garden meter** can save money. **Ask the utility.**
- **Restrictions:** in dry seasons some regions limit garden watering.

## Tools
Spade or trencher (rent), pipe cutter, deburring tool, wrenches, PTFE tape, spray paint, a bucket and a stopwatch, a pressure gauge, a multimeter, cable strippers, waterproof wire connectors, a compressor and regulator for winterising.

## Common mistakes
- **No flow measurement:** too many heads per zone, weak spray, no pressure.
- **No backflow preventer.**
- **No drain points,** so frost cracks the pipes and valves.
- **No sleeves** under paving, then digging it up.
- **No filter** on a drip system.
- Watering **a little every day** (shallow roots) instead of deeply and rarely.
- **No plan of the buried pipes.**

## Quality checks
- **Each zone's coverage** checked with cans (a uniform depth after a run), **no leaks** at the fittings, pressure at the end head within the head's range.
- **Controller schedule** and the rain sensor tested, **winterising routine** written down.

## Cross-trade
- Garden groundwork (sleeves, levels), terraces and paving, smart home (controller and sensors), electrical (outdoor-rated, RCD, licensed), pool (filling water and the water meter), region file (water rules).

## Element: supply connection, backflow, filter and regulator
1. **Position** at the **tap or a dedicated connection** with an **isolation valve**, and **a drain point**.
2. **Order of parts** (flow direction): **isolation valve → backflow preventer → filter (120–150 mesh for drip) → pressure regulator (≈ 1–1.5 bar for drip) → the manifold**.
3. **Backflow preventer** where the rules require it (**many countries**), **above the highest outlet** if it is the atmospheric type.
4. **Install** with **unions** for service, **check the flow direction arrows**, **no leaks**.

## Element: main line and valve manifold
1. **Trench** ≈ 25–40 cm deep (deeper for the main in frost areas), **sloping to a drain point**.
2. **Main:** **PE pipe 25–32 mm** with **compression fittings**, **a shut-off valve** at the manifold.
3. **Valve manifold:** **one 24 V solenoid valve per zone**, **in a valve box with gravel under it**, **the wires with waterproof connectors** and **a spare pair**.
4. **Flush the main** before connecting the laterals. **Draw** the pipe route.

## Element: controller, wiring and sensors
1. **Controller** indoors or in a weather-proof box, **24 V transformer**, **power by a licensed electrician (RCD)**.
2. **Wiring:** **24 V multi-core cable** (one common + one per valve + spares), **buried in conduit**, **labelled at both ends**.
3. **Sensors:** a **rain sensor** (and optionally a **soil moisture or a flow sensor**). **Program** the zones, **start times in the early morning**, **a seasonal adjustment**.
4. **Smart control** by Wi-Fi or a hub if wanted (`smart-home.md`), **a manual run** always possible.

## Element: sprinklers (lawn)
1. **Head-to-head spacing** (the spray reaches the next head), **matched precipitation** within a zone (rotors with rotors, sprays with sprays), **a pressure within the head's range**.
2. **Heads** at the **lawn's finished level** (**flush**), **adjusted arc and radius**, **a check valve** in low spots against drainage.
3. **Zones:** **demand ≤ 70–80% of the flow**. **Run time** from the precipitation rate.
4. **Test** each zone (**catch cans** for an even distribution).

## Element: drip lines (beds, trees, hedges)
1. **Pressure regulator and a filter** (mandatory).
2. **Main drip tube** (16 mm) with **drippers or an integrated dripline** (typically **2–4 l/h per emitter**), **spacing as the plant needs**, **pegged and mulched**.
3. **Trees:** **a ring of drippers or a loop** around the root ball, **a few more as the tree grows**.
4. **Flush** the ends with **end caps** at the start of each season, **check for clogs and animals**.

## Element: rain tank and pump
1. **Tank** (≥ 1–5 m³), **a gutter filter, a first-flush diverter** if needed, **a covered, dark tank**, **an overflow to a soakaway or drain**.
2. **Pump** with a **pressure switch** and a **check valve**, **a float intake** just below the surface.
3. **No cross-connection** with the drinking water (**air gap or a separate tap**), **labelled "not drinking water"**.
4. **Frost:** **drain or insulate**, **winter the pump**.
