# Trade: Indoor stairs (inspection, repair, refinishing, replacement)

Graph tasks: `indoor-stairs-inspection`, `indoor-stairs-work`. Local rules differ: check the region file for the **rise, going, headroom, handrail and guard** rules. Typical values below. For outdoor stairs see `outdoor-stairs.md`.

**DIY level:** inspection, repair of creaks, refinishing, new treads and handrails, and installing a **stair kit** are DIY for a careful person. **Engineer and permit** for new openings in the floor, cutting joists, and changing a stair's position or type in a way that affects the structure. **Falls on stairs are a leading cause of home injuries.**

## Inspection checklist (task: `indoor-stairs-inspection`)
Measure and write the results in the room file.
1. **Geometry:** rise (riser height) R and going (tread depth) T of **every step**, and the differences. Use a long level and a tape. **Typical comfort ranges:** R ≈ 17–19 cm (max ≈ 19–20 cm), T ≈ 25–30 cm, **2R + T ≈ 59–65 cm**. **Differences between steps ≤ ≈ 5 mm.**
2. **Headroom:** vertical clear height from the nosing line (typically **≥ 2.0–2.1 m**). Check at the opening above and any beams.
3. **Width:** typically **≥ 80 cm** (better 90–100 cm), landings at least as deep as the stair is wide.
4. **Structure:** push and bounce each tread (**creaks, sag, movement**), look under for **cracked or split stringers, loose or missing wedges and glue blocks, woodworm, rot, rusty fixings, gaps at the walls**. For concrete or steel: cracks, rust, loose cladding.
5. **Handrail and guard:** **push test** at several points (a firm horizontal push), height **≈ 90–100 cm**, **openings ≤ 12 cm (≤ 10 cm with small children)**, no horizontal rails that can be climbed, the ends secure.
6. **Surface:** worn or loose nosings, carpet or vinyl lifting, slippery varnish, missing non-slip strips.
7. **Light and switches:** light on every step, **switches at both ends**, a night light.
8. **Escape and fire:** is the stair a protected escape route (doors, enclosed stairwell, smoke detector)? Is it cluttered?
9. **Sound:** impact noise to the rooms below.
10. **Rise from floor to floor:** measure the **finished floors** upstairs and downstairs. **A planned floor build-up change alters the first and last riser** (see below).
- **Verdict:** safe as is, **repair**, **refinish**, or **replace**. **Stop use** and block access if a stringer, post or tread is cracked or loose.

## Types and geometry
- **Straight**, **L-shaped or U-shaped with a landing**, **quarter or half winders** (turning steps: the going at the **walking line (≈ 40–50 cm from the narrow side)** must meet the rule, and the **narrow end ≥ ≈ 10 cm**), **spiral** (small footprint, often only as a secondary stair), **open riser** (gap ≤ 12 cm, or ≤ 10 where children), **closed riser**, floating stairs (steel or concrete stringers, wall-fixed).
- **Calculation (new or changed floors):** n = total rise ÷ R, rounded. Then R = total rise ÷ n. Example: floor-to-floor 2.80 m ÷ 0.175 ≈ 16 steps → R = 17.5 cm. The number of goings is n − 1 (the top floor is the last tread). Total run = (n − 1) × T.
- **Opening:** the floor opening must provide the headroom along the whole stair.

## Where it goes wrong: floor levels
**Every floor covering changes the total rise.** Adding 15 mm parquet and 5 mm underlay on the upper floor and 10 mm tiles on the lower floor changes the first and the last riser by 20–30 mm, **more than the 5 mm tolerance**. Fix by:
1. **Doing the stair calculation with the finished floors** (`finished_floor_level` in the graph).
2. Adjusting the **first and last step** (build-up under the first tread, or a levelling layer on the landing) so all risers match.
3. Never "fixing" it by making one step different. That is the trip.

## Repair and refinish (task: `indoor-stairs-work`)
- **Creaks:** find the moving part (two people). Fix with **screws from below** (pre-drilled, into the stringer), **glue blocks** at the tread and riser, **re-wedged and glued wedges**, or screws through the tread into the stringer (countersunk and plugged). Dry lubricant (talc) only as a temporary fix.
- **Loose treads or risers:** re-glue (PVA or PU wood glue, clamped), add screws, **replace** a damaged tread (a kit of the same thickness).
- **Refinish wood stairs:** remove old varnish or oil (sanding with an orbital sander, grit 80 → 120 → 180), fill cracks, **vacuum thoroughly**, apply oil or hard-wearing waterborne lacquer in thin coats with a **non-slip finish or additive**. **Block the stair while it cures** (a few days). Use the other stair or a second route.
- **Cover or clad old stairs:** step-cladding kits (laminate, vinyl, hardwood overlays) onto sound treads. Check the **nosing profile** and the **riser heights** (cladding adds to the tread and the riser: keep every step equal).
- **Carpet:** use stair rods or glued grippers. No loose carpet on stairs.
- **Non-slip:** adhesive strips or inserted nosings, a contrasting nosing edge, and good light.
- **Handrail and guard replacement:** fix **posts to the stringers or the floor structure** with through-bolts or lag screws (**not into plasterboard**), a **wall handrail** on **solid brackets into studs or masonry** every ≈ 80–100 cm, **balusters spaced ≤ 12 cm**, and the **handrail continuous**.
- **New stair (kit):** measure the total rise and the opening precisely, order the kit with the **correct rise per step**, fix the **top connection** into the structure (trimmer joists, engineer for a new opening), the foot on the finished floor, and the **handrail to the code**. Typical time 1–2 days for two people.
- **New opening in a floor:** **engineer, permit and trimming of joists.** Not DIY without the design.

## Tools
Tape measure, long level, laser, set square, drill/driver and countersink, clamps, wood glue, orbital sander and hand sanding block, chisels, saw, mallet, vacuum, brushes, roller, masking tape, a stud finder, a plumb line, gloves, safety glasses, FFP2 mask for sanding, ear protection.

## Common mistakes
- Changing floor coverings without recalculating the first and last risers.
- Risers differing by more than a few millimetres.
- A handrail fixed into plasterboard, or a loose balustrade.
- No light, or no switch at one end.
- Slippery finish (high-gloss lacquer) with socks and children.
- A loose stair carpet.
- Cutting a stringer or a joist without an engineer.

## Quality checks
- Risers within ≈ 5 mm, goings within ≈ 5 mm, headroom as measured, no creaks, no movement of the handrail under a firm push.
- Lighting and switches work from both ends.

## Cross-trade
- **Flooring and floor levels** (`flooring.md`, `screed.md`), hallway (`rooms/hallway.md`), attic conversion (`roof.md`), painting (`painting.md`), electrical (stair lighting, switches), fire safety (escape routes, smoke detectors), permits.

## Element: measuring the stair
1. **Tools:** a long level, a tape, a notepad, a **plumb line**. **Make a table** of every step: **rise (R)** and **going (T)**.
2. **Find the differences** (**≤ ≈ 5 mm** within the flight). **Mark the worst steps.**
3. **Headroom:** the vertical clear height **above the nosing line** (≥ ≈ 2.0–2.1 m). **Width** and **landing size**.
4. **Total rise** floor to floor **with the finished floors** (or planned) and **the number of steps**.

## Element: creaks and loose treads
1. **Find** the moving part with **two people** (one steps, one watches and listens below).
2. **From below:** **glue blocks** at the tread and riser, **re-wedge and glue** the wedges, **screw upward** through the stringer into the tread (**pre-drilled**).
3. **From above:** **countersunk screws** through the tread into the stringer, **plugged or filled**, **wood glue in the joint**.
4. **Carpeted stairs:** **lift the carpet** and **screw** through the tread, then **refit**.
5. **Fill gaps** with **wood glue and slivers**. **Test** after 24 h.

## Element: replacing a tread or riser
1. **Measure and buy** a tread of the **same thickness, width and nosing profile**.
2. **Release** the old one (**cut the nosing and the fixings** with an oscillating tool, **lift out**).
3. **Clean** the seat, **dry-fit** the new tread, **glue** (wood glue + screws from below), **clamp or weigh down**.
4. **Match the finish** (stain and varnish) **before** fitting if possible.
5. **Check** the rise stays equal (**same thickness**).

## Element: balustrade and handrail
1. **Posts:** **through-bolted or lag-screwed** into the **stringers or the floor structure** (**never into plasterboard**), **plumb**.
2. **Handrail:** **≈ 90–100 cm** over the nosing line, **continuous**, **40–50 mm grip**, **ends returned** to the wall or posts. **Wall handrail** on **brackets every ≈ 80–100 cm into studs or masonry**.
3. **Balusters:** **spacing ≤ 12 cm** (≤ 10 cm where small children live), **no horizontal rails** that can be climbed.
4. **Push test** at several points (a firm horizontal load), **no wobble**.

## Element: refinishing the treads
1. **Remove** the old finish (an **orbital sander** 80 → 120 → 180 grit, **hand-sand** the corners), **vacuum**.
2. **Repair** dents and gaps (wood filler or slivers).
3. **Finish:** **hard-wearing oil or waterborne lacquer** in **thin coats** with **a non-slip additive or a satin finish**. **Sand lightly** between coats.
4. **Block** the stair while it cures (a few days) and **use another route**.
5. **Non-slip** strips or inserted nosings if the surface is slippery.

## Element: stair lighting
1. **Light on every step** (low-level wall lights or **LED strips under the nosing**), **even light**, **no glare**.
2. **Switches at both ends** (two-way), **a presence sensor** for the night.
3. **Cables** laid in the rough-in (**low-voltage strips with a driver**), **fixtures last**, by the electrician for mains.
