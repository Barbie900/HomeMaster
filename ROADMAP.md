# Roadmap

Built step by step. Each step is usable on its own.

## ✅ Step 1 — Skeleton
- Plugin manifest + marketplace (installable via `/plugin`)
- Knowledge skill with answer principles, output format, glossary, region notes
- Dependency graph schema + bathroom seed (`dependencies.yaml`)
- `/homemaster:new-project` interview + project templates
- Core agents: `project-lead`, `dependency-checker`, `safety-reviewer`

## ✅ Step 2 — Bathroom trade knowledge (first draft, needs field test)
One reference file per trade in `skills/knowledge/references/trades/`, each with: materials (with standard classes), tools (have / buy / rent), method, tips, mistakes, waiting times, quality checks, cross-trade links.
- demolition · plumbing & drainage (incl. sanitary fit-out) · electrical (zones, IP, RCD) · ventilation
- screed & levelling · underfloor heating · waterproofing · drywall in wet areas · walls & ceilings · carpentry
- tiling (layout, adhesives, large-format, grouting, silicone)
- Quantity formulas in `references/quantities.md`

> Values are "typical" and marked as such. **Needs review by a professional tradesperson per trade** and a real bathroom field test (step 5).

## ✅ Step 2b — Whole home (first draft, needs field test)
- 10 room-type guides in `references/rooms/`: bathroom, kitchen, living room, bedroom, hallway, basement, outdoor stairs, terrace, wellness, other
- House-wide planning in `references/trades/planning.md`
- New trades: flooring, painting and skim, kitchen, windows, insulation, basement moisture, outdoor surfaces, outdoor stairs, wellness
- Graph extended with 25 generic tasks (42 in total) for the whole house (permits, panel, heating plan, insulation, windows, wall finish, painting, floors, kitchen, basement, outdoors, wellness)
- Added: roof and attic, facade (ETICS and render), garden structures, pools, indoor stairs (5 more room types, 5 more trade files, 14 more graph tasks)
- Added: chimney and stove, garden and landscaping, irrigation, outdoor pool (siting, heating, winter), smart home (4 more trade files, 5 more room types, 12 more graph tasks)
- Not covered yet: wet-room accessibility, electrical panel work (by design a professional's job), PV, battery and EV charger installation in depth (only planning and links), new-build structure, garage and workshop in depth

## ✅ Step 2c — Work packages (first draft)
- `references/packages.yaml` (206 work packages) and `references/sequences.yaml` (an ordered list for every room type: bathroom 45 steps, kitchen 47, living room 49, bedroom 43, hallway 43, basement 38, roof and attic 32, wellness 24, facade 21, garden 20, smart home 18, ...)
- **Element-level sections for all rooms:** floors (6), painting (6), electrics for dry rooms (5), doors, skirting, wardrobe, mat well (5), windows (3), kitchen (8), basement (5), outdoor stairs (4), terrace and decking (9), wellness (8), roof (5), facade (9), garden structures (6), pool (7), indoor stairs (6), chimney (6), landscaping (3), irrigation (6), smart home (8)
- New element-level knowledge: `sanitary.md` (WC frame and bowl, shower drain, basin, fixtures, **shower glass**, bath), `water-heating.md`, drain lines, supply lines and tests in `plumbing.md`, radiators and towel rails in `heating.md`
- Skills `/homemaster:plan-room` and `/homemaster:next-step` (one work card at a time, with dependency check, plan and log updates)
- Validation script for the order of every sequence

## ⬜ Step 3 — Core workflows
- ✅ `/homemaster:plan-room`: ordered plan for a room (written, needs field test)
- ✅ `/homemaster:next-step`: one work package at a time (written, needs field test)
- Trade specialist agents (tiler, plumber, electrician, waterproofing, drywall)

## ⬜ Step 4 — Decisions & purchasing
- `/homemaster:compare`: options compared with a recommendation for this project
- `/homemaster:shopping`: material quantities (with waste %), consolidated tool list (have / buy / rent)
- `/homemaster:log`: record progress; downstream tasks get dated "earliest start"

## ⬜ Step 5 — Field test
- Run a real bathroom end to end and fix gaps in the knowledge

## ⬜ Step 6 — More rooms & trades
- Kitchen · floors (laminate, parquet, vinyl) · walls & painting · ceilings · windows & doors · heating · insulation · exterior

## ⬜ Step 6b — Web chat version (claude.ai)
- Plugins don't load in the claude.ai web chat. Options: (a) the knowledge and the `plan-room` / `next-step` skills packaged as uploadable **skills**, (b) a **Project** with the knowledge files and instructions. Both need the project data (`my-home/`) to live in the chat or in a file the user uploads.

## ⬜ Step 7 — Publish
- Public GitHub repo, contribution guide, example project, more languages
