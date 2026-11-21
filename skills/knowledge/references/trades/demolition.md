# Trade: Demolition and strip-out

Graph tasks: `demolition`. Values are typical: check the product data sheet and local rules.

**DIY level:** fully DIY, with the safety checks below done first. Hard work, not difficult work.

## Before you swing anything (all are in the graph as `critical`)
1. **Water off and lines drained**: close the stopcock, open the lowest tap. In apartment blocks you may need the building manager to close the riser.
2. **Power off at the panel and verified dead** with a voltage tester on every socket, switch and light in the room. A switch off is not proof. Label the breaker.
3. **Load-bearing check.** Don't remove or chase walls you haven't confirmed as non-load-bearing. A 10 cm masonry wall can be load-bearing.
4. **Asbestos / hazardous materials.** Houses and blocks from before ~1995: asbestos-cement boards, old floor tiles (vinyl/"floor flex"), tile adhesive and pipe lagging can contain it. If in doubt: stop, don't break, drill or sand it, and have a sample taken and tested by an accredited lab (the region file says who may take it). Asbestos removal is regulated.
5. **Kit for living in the home:** a second toilet/shower, plastic and tape to seal the doorway, drop cloths on the route out, floor protection in the hallway.

## Tools
| Item | Have / buy / rent | Notes |
|---|---|---|
| SDS-plus hammer drill with chisel function (≈ 3–5 kg) | rent or buy | for walls and tiles. Floor tiles with an SDS-max (≈ 5–10 kg) are faster and need less effort, but use a lighter one on slabs in apartment blocks |
| Flat chisel 40–50 mm and pointed chisel | buy | change when dull. A dull chisel doubles the time |
| Hand sledgehammer 1.5–3 kg, cold chisel, crowbar | have/buy | |
| Angle grinder 125 mm with diamond blade | have | for cutting screed into sections and for chases (with a dust shroud) |
| Wall chaser (two-blade) | rent | cleaner and straighter chases than a grinder, with an extraction port |
| M-class dust extractor | rent/buy | silica dust. Connect to the chaser or hammer shroud |
| FFP3 mask, goggles, ear defenders, gloves, safety boots, knee pads | buy | non-negotiable. FFP2 is not enough for silica |
| Heavy-duty rubble bags, wheelbarrow, sack truck | buy | |
| Skip / container or collection-centre trips | arrange | see region file |

## Method
1. **Photograph everything** first: pipes, cables, junction boxes, the stack position. Measure and sketch positions of anything you'll keep.
2. **Order of removal:** fixtures and furniture → ceiling lights/trims → wall tiles (top to bottom) → floor tiles → floor build-up (screed) only if you decided to remove it.
3. **Disconnect safely:** cap water pipes with proper end caps, disconnect and cap drains and stuff cloth/plug into open drains to stop gas and debris. Terminate cables in a junction box (no loose ends under walls).
4. **Wall tiles:** chisel at a shallow angle (≈ 20–30°) into the joint, work top-down. Hold the chisel and don't lever against the plaster. Expect plaster to come off with the tiles on old walls.
5. **Floor tiles:** break one tile in the middle, then work from the hole with the chisel under the edge of the neighbouring tile. Keep the hammer on low impact or chisel mode. Don't gouge into the slab.
6. **Screed removal (only if needed):** cut a grid of ≈ 50 × 50 cm with a diamond blade to the full depth *except where heating pipes or the slab could be hit*, then break out the squares. Floating screed on insulation comes up with a crowbar once cut.
7. **Chases:** mark the route (straight, horizontal/vertical only), cut both edges with the chaser, remove the web with a chisel. In masonry keep chases shallow; **in load-bearing walls, depth and length are limited by structural rules — ask an engineer.**
8. **Clean:** vacuum with the M-class extractor (never sweep dry), then wipe. Silica dust settles for hours.
9. **Re-inspect the substrate** (see Quality checks).

## Tips & tricks
- Damp the debris lightly with a spray bottle to keep dust down. Don't flood electrics.
- Tile rubble is heavy: ≈ 1.5–2 t per m³ loose. Fill bags only half. A 6 m² bathroom (tiles + adhesive + 5 cm screed) is roughly **1–1.5 tons**. Plan the container size and neighbours' parking.
- Take down the **door** and protect the frame with cardboard if it stays.
- Do noisy work only in allowed hours. Tell the neighbours below.
- Measure and note the old WC outlet position and the stack height before you remove the pan. You need them for the new layout.

## Common mistakes
- Hitting hidden pipes or cables: use your photos, and a cable/metal detector if the previous work isn't documented.
- Not sealing the doorway: dust gets into the entire home.
- Cutting grooves in the floor slab or in beams: ask before cutting anything structural.
- Not checking asbestos before demolishing.

## Quality checks (after strip-out)
- Walls: sound, no loose plaster (tap test: hollow sound = remove), no active damp (hygrometer or moisture meter with calibrated reading, not by feel).
- Slab: level, no cracks that move, no hollow areas. Measure the heights at the door and at the stack to plan the floor build-up.
- **Record the dimensions and the existing floor height** in the room file. All later quantities depend on them.

## Cross-trade
- Plan the finished floor level (FFL) now: mark the reference line on every wall *before* the rough-in (graph: `reference_lines`).
- Stack position and pipe sizes decide where the WC can go: look before you buy the sanitary items.
- If you discover asbestos, hollow plaster or damp, update `profile.md` and re-run the safety review.
