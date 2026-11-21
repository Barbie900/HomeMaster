# Trade: Wellness (sauna, steam room, hot tub)

Graph tasks: `wellness-plan`, `sauna-build`, `steam-room-build`. **High-risk area.** Manufacturer instructions, the electrical rules and fire rules win. All electrical connections by a licensed electrician.

**DIY level:** a **pre-fabricated sauna kit** or a **built-in cabin shell** (framing, insulation, vapour barrier, cladding, benches) is DIY. **Not DIY:** the heater and generator connections, the electrical installation, gas or wood-fired heaters, pool structures and hot-tub electrics.

## Choose
| Option | What it is | Notes |
|---|---|---|
| **Finnish sauna** | 70–100 °C, dry (10–25% RH), electric stove with stones | needs 6–9 kW (usually 3-phase), a good ventilation design |
| **Infrared cabin** | 40–60 °C radiant panels | 1.5–3 kW, plug-in (check circuit), low complexity |
| **Steam room (hammam)** | 40–50 °C, ≈ 100% RH, tiled | steam generator, steam-tight room, ceiling slope, drain |
| **Hot tub (indoor)** | 36–40 °C water | weight ≈ 1.5–2.5 t filled, humidity, drain, RCD, equipotential bonding |
| **Small indoor pool** | water volumes and chemistry | **specialist project** (structure, waterproofing, dehumidification, plant) |

## Planning (task: `wellness-plan`)
- **Capacity and power:** the heater or generator may need a **3-phase supply** (6–9 kW). Check the connection and the panel with `panel-and-main-services`.
- **Floor load and structure:** an engineer for hot tubs and pools. Concrete slab on ground is the simplest.
- **Waterproofing and drainage:** a floor drain or a tray, falls to the drain. Steam rooms need steam-tight membranes on all surfaces.
- **Ventilation and humidity removal** for the room around it: an extract fan or a dehumidifier. Wet air must not go into walls.
- **Escape and fire:** the cabin door opens outward, no lock, a safe route out, smoke or heat detectors in the surrounding room. Insurance and local rules.
- **Hot water, shower and cooling area** nearby. Toilets and relaxation are part of the design.

## Sauna cabin construction (task: `sauna-build`)
**Layers from the inside out:** cladding (spruce, aspen, alder, cedar; 12–16 mm tongue-and-groove boards) → **battens (≈ 20 mm air gap)** → **reflective aluminium vapour-barrier foil, taped at all joints (warm side)** → **mineral wool insulation 50–100 mm (non-combustible, heat-rated)** between the frame studs → wall frame or the masonry wall. **No foam insulations** in the cabin, and no ordinary PE film.
- **Dimensions:** ceiling height ≈ 2.1–2.3 m. **Upper bench seat ≈ 100–110 cm above the floor**, depth ≈ 60 cm, lower bench ≈ 50 cm lower, clearances around the heater per the maker. **≈ 0.8–1 m² of floor per person.**
- **Heater size:** about **1 kW per m³ of cabin volume**, plus the heater maker's allowance for glass and uninsulated or tiled surfaces (≈ 1.2 kW per m² of glass, typically).
- **Heater:** rated for the room volume, safe clearances to combustibles per the maker, **temperature limiter, heat-protective barrier or rail**, stones filled per the maker. **No object** on or close to the heater.
- **Ventilation:** **fresh air inlet low near the heater**, **exhaust high on the opposite side** (≈ 6 air changes per hour, per the maker). Keep the vents unobstructed. The room outside the cabin needs ventilation too.
- **Electrical:** **heat-rated cables (e.g. silicone-insulated, ≥ 170 °C) and sauna-rated fittings and lights**, a separate circuit with RCD, an **emergency isolating switch** outside. Installed and measured by the electrician.
- **Door:** tempered glass or a wooden door with an outward swing, **no lock**, magnetic catch. **Floor:** tiles on waterproofing with a drain, or a concrete floor with removable duckboards.
- **Fire safety:** don't dry clothes on or near the heater. Install a heat detector in the cabin vestibule and a smoke detector outside.

## Steam room (task: `steam-room-build`)
- **Steam-tight shell:** all walls, **ceiling** and floor waterproofed with a membrane rated for permanent wetness and steam, with tape and collars. Tiles and joints must resist heat and moisture (C2 S1 adhesive and epoxy or a rated grout).
- **Ceiling sloped ≥ 5° (10–15° is better)** towards a wall so condensate runs off instead of dripping onto bathers. **Round the corners** where practical.
- **Steam generator:** sized to the cabin volume and surfaces (≈ 1 kW per m³ for tiled cabins, more for glass or stone, per the maker's tables). **Place it outside the cabin** with an insulated, falling steam pipe. **Steam outlet ≈ 30–50 cm above the floor and away from seats** (burn hazard).
- **Floor drain and falls** (1–2%) to the drain. **Seat slope** ≈ 5° forwards so water runs off. **Rounded benches.**
- **Door:** glass (tempered) with a seal, **outward swing, no lock**. **Ventilation**: an extractor outside the cabin and a slow ventilation (dry out after use).
- **Temperature limiter** and a safe control. The electrics follow the same rules as the sauna.

## Hot tub (indoor)
- **Weight:** floor load check (≈ 1.5–2.5 t filled), a stiff, flat slab, and **a level base** per the maker.
- **Water:** hot tub drain and a floor drain in the room, **waterproofed floor**, **humidity removal** (an extractor or a dehumidifier), and **an RCD circuit with equipotential bonding** (licensed electrician).
- **Access:** space for the filter and service panels, a cover, a safe floor surface, **slip-resistant tiles (class B or C wet barefoot)**.

## Tools and PPE
As for tiling, drywall and carpentry, a vapour-barrier tape, a stapler, a cutting knife, and a long straightedge. **Mineral wool:** a mask FFP2, gloves, goggles. **Never** operate a new heater without the first test run (with the maker's instruction: a first heat-up at an open window, to burn off residue).

## Common mistakes
- Using the wrong vapour barrier, or leaving it untaped.
- Foam or flammable insulation, non-heat-rated cables or lights in the cabin.
- Heater too small (slow, wet) or too large (dangerous temperatures at the ceiling).
- No inlet vent, or the vent blocked.
- A flat steam-room ceiling, wet drips.
- A door with a lock.
- Forgetting the weight of a hot tub.
- Humid air leaking into the structure around the cabin.

## Quality checks
- Cabin and electrics inspected and measured by the electrician. Heater and limiters tested.
- Moisture in adjacent rooms is under control (hygrometer).
- No condensation drips in the steam room, correct falls and drain flow.

## Cross-trade
- Electrical (panel capacity, licensed work), plumbing (drain, water), waterproofing and tiling, ventilation (humidity removal), structure (floor loads), insurance.

## Element: electrical supply and heater (licensed)
1. **The electrician plans:** the **heater's power** (≈ 1 kW per m³ plus the maker's corrections), **three-phase supply** if 6–9 kW, **cable size, breaker, RCD**, **a separate isolating switch outside the cabin**, **heat-rated cable** inside.
2. **You prepare:** the **conduit route**, the **space and the backing** for the control unit, the **photographs**.
3. **Heater placement:** **clearances to combustibles per the maker**, a **protective barrier** around it, **stones filled as the maker says**, **never an object on the heater**.
4. **Test:** the **limiter and the thermal cut-out**, the **first heat-up** per the sheet (with ventilation, to burn off residue).

## Element: floor, drain and waterproofing (wellness)
1. **Floor falls ≥ 1–2%** to a **floor drain** or a tray. **Waterproofing** as `waterproofing.md`, up the walls ≥ 20 cm.
2. **Sauna cabin floor:** **tiles on waterproofing** or **concrete**, **removable duckboards**, **a threshold that doesn't trap water**.
3. **Steam room:** **all surfaces including the ceiling** waterproofed (steam-tight), **tape and collars** at each penetration.
4. **Test:** flood or sprinkle test before tiling or cladding.

## Element: frame, insulation and vapour barrier (sauna)
1. **Frame:** studs at ≈ 40–60 cm, **no gaps** to the masonry (or free-standing in the room).
2. **Insulation:** **non-combustible mineral wool 50–100 mm** between studs, **no foam**.
3. **Vapour barrier:** **reflective aluminium foil** (the warm side), **every joint overlapped (≥ 5 cm) and taped with aluminium tape**, **sealed around boxes and penetrations**.
4. **Battens ≈ 20 mm** on the foil for the **air gap** and the cladding, **no gaps** in the foil.
5. **Photograph** before cladding.

## Element: cladding and benches (sauna)
1. **Wood:** spruce, aspen, alder or cedar **12–16 mm tongue-and-groove**, **stainless or hidden fixings**, **no knots in bench boards**, **no varnish**.
2. **Cladding:** **horizontal on walls**, **the ceiling first**, **a gap of 5–10 mm** at the ceiling and the floor for ventilation.
3. **Benches:** **upper bench seat ≈ 100–110 cm**, depth ≈ 60 cm, **lower bench ≈ 50 cm lower**, **rounded edges**, **removable slats**, **fixed to the frame**, **no metal fixings on the surface**.
4. **Backrests** and a **head rest**, **heater guard**.

## Element: door and glass (wellness)
1. **Door:** **tempered glass 8 mm** or a wooden door, **outward-opening**, **no lock**, a **magnetic or roller catch**, **hinged on the side that keeps the escape free**.
2. **Fixed glass:** **tempered**, **fixed in profiles**, **sealed with heat-resistant silicone**.
3. **Test** that the door **opens from the inside with a light push**.

## Element: cabin ventilation
1. **Inlet** at the **bottom near the heater**, **outlet** at the **top on the opposite side** (or the maker's design), **≈ 6 air changes per hour**.
2. **Vents not blocked**, **adjustable**, **screens**.
3. **The room around** needs its **own ventilation and dehumidifying** (`ventilation.md`).

## Element: steam generator and outlets
1. **Generator** outside the cabin, **sized** per the maker's table (≈ 1 kW per m³ for a tiled cabin, more for glass or stone), **water supply and drain**, **descaling plan** (hard water).
2. **Steam pipe** **insulated, falling continuously** to the cabin, **outlet ≈ 30–50 cm above the floor, away from seats**, a **temperature sensor ≈ 160 cm** high.
3. **Ceiling slope ≥ 5° (10–15° better)**, **drip edges**, **benches sloped ≈ 5°** forward.
4. **Test:** a **first run** with a **leak check at the pipe joints** and a **temperature check at seat height**.

## Element: hot tub placement
1. **Base:** a **flat, reinforced slab** (≈ 12–15 cm concrete or the maker's value) **or a floor engineer-checked for ≈ 1.5–2.5 t**.
2. **Drain and floor drain** in the room, **waterproofed floor**, **humidity control**.
3. **Electrical:** a **dedicated circuit with RCD**, **equipotential bonding**, a **disconnect within sight** (licensed electrician).
4. **Access** for the filter and panels, **a cover**, **non-slip surround**.
