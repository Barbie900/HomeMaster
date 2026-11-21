# HomeMaster 🏠🔨

**A Claude Code plugin that plans a full DIY home renovation — room by room, with connected knowledge.**

🇸🇮 [Slovenska navodila → README.sl.md](README.sl.md)

Most renovation advice is siloed: a tiling guide doesn't know your screed was poured last week, and a plumbing guide doesn't know where your finished floor will end up. HomeMaster connects the trades. Before it writes instructions for a task, it checks a **dependency graph** and **your project log**, and warns you about anything another trade affects.

> Example: you ask for floor-tiling instructions. HomeMaster checks your log, sees the screed went down 12 days ago over underfloor heating, and **stops you**: the screed needs a CM moisture test (≤ 1.8 CM-% for heated cement screed) and a heating-up protocol first. Then it gives you the full instructions with the exact tools, materials, quantities, tricks and the checks to do along the way.

## What you get

| | |
|---|---|
| 🧭 **Project setup** | An interview about your home (house / flat / cottage, year built, construction, budget, skills, tools you own) |
| 🔗 **Dependency graph** | Every task knows what has to be done before it, what it blocks and what can go wrong between trades |
| 📋 **Work instructions** | Preconditions, tools (have / buy / rent), materials with quantities and waste, steps, tips, common mistakes, drying times, quality checks |
| ⚖️ **Recommendations** | Compares options (e.g. liquid membrane vs. sheet waterproofing) and says which is better *for your case* |
| 🦺 **Safety reviewer** | Flags work that legally or practically needs a professional (gas, electrical certification and measurements, load-bearing walls, asbestos) |
| 🗒️ **Project memory** | A log of what's done and when, so later advice builds on it |

## How you work with it: small steps, in order

Instructions for a whole room would be far too long. HomeMaster splits every room into **work packages** and keeps the order:

1. `/homemaster:plan-room`: the ordered list for your room (for a bathroom: drains, WC frame, shower drain, supply lines, hot water, tests, screed, waterproofing, tiling, WC bowl, basin, shower, glass, ...), with waiting times, who does what, and what to book first.
2. `/homemaster:next-step`: **one package at a time** as a short work card (tools, materials, steps, checks), after a check that everything before it is done.
3. Tell it when a step is finished. It updates the plan and the log and unlocks the next one.

## Install

In Claude Code:

```
/plugin marketplace add Barbie900/HomeMaster
/plugin install homemaster@homemaster
```

Then create a **separate folder for your home** (never inside the plugin), open Claude Code there and run:

```
/homemaster:new-project
```

## Where you can use it

HomeMaster is a Claude Code plugin, so it runs wherever Claude Code runs, not only in a terminal:

| Where | How |
|---|---|
| **Claude desktop app, Code tab** (a normal chat window) | Start a session in **your home folder**, then type `/homemaster:new-project`. |
| **VS Code / JetBrains extension** | Open your home folder, open the Claude panel, type `/homemaster:new-project`. |
| **Terminal** | `cd` into your home folder, run `claude`, type `/homemaster:new-project`. |

You install the plugin once (see above). After that you can just talk to it in plain language ("I want to renovate my bathroom", "what is the next step?"). The slash commands are only shortcuts.

> **claude.ai in the web browser** does not load Claude Code plugins. A version for the web chat (skills or a Project) is on the [roadmap](ROADMAP.md).

## Language

The plugin's structure and knowledge base are in English so anyone can contribute. **Agents answer in the language set in your project profile.** Slovenian ships with a glossary and regional notes (`skills/knowledge/references/regions/`). Adding a language means adding a glossary and a region file. See [docs/CONTRIBUTING.md](docs/CONTRIBUTING.md).

## Status

Early development. HomeMaster plans a **whole home**, with a dedicated guide for each room type:

| Room type | Covered |
|---|---|
| Bathroom and WC | most detailed (waterproofing, screed, tiling, electrical zones) |
| Kitchen | layout, services, extraction, fitting |
| Living room, bedroom, hallway | floors, painting, heating, acoustics, safety |
| Basement | moisture diagnosis, waterproofing, radon, conversion |
| Outdoor stairs, terrace | geometry, frost, drainage, tiles, paving, decking, handrails |
| Wellness | sauna, steam room, hot tub (planning and building rules) |
| Roof and attic | inspection, safe working, small repairs, attic conversion |
| Facade | insulation system (ETICS), render, repairs, scaffold and permits |
| Garden structures | shed, pergola, carport, fence, retaining wall, foundations |
| Pool | planning, structure, filtration, safety, chemistry (electrics always licensed) |
| Indoor stairs | inspection checklist, repair, refinishing, replacement, floor-level effects |
| Outdoor pool | siting, heating and cover, natural pond, swim spa, winter routine |
| Chimney, stove, fireplace | inspection, flue, hearth, combustion air, safe operation (sweep signs off) |
| Garden and landscaping | survey, soil, lawn, beds, trees, hedges, order of work |
| Irrigation | flow and pressure, zones, drip and sprinklers, backflow, winterising |
| Smart home | cabling in the rough-in, standards, local control, security and privacy |
| Other (office, utility, garage) | mapped to the closest type |

Plus **house-wide planning**: order of phases and rooms, shared decisions (panel, heating, insulation, windows), living in the home, budget and lead times.

Everything is a **first draft** and needs review by tradespeople and a real project. See [ROADMAP.md](ROADMAP.md).

## ⚠️ Disclaimer

HomeMaster gives guidance, not a guarantee. Always follow the product manufacturer's data sheets, local building codes and regulations. Gas, connection to the grid, certification of electrical installations and structural changes need licensed professionals in most countries. You are responsible for your own safety.

## License

MIT
