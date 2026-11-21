---
name: new-project
description: Start a new HomeMaster renovation project in the current folder. Interviews the user about their home (house, flat or cottage, construction, rooms, budget, skills, tools) and creates the my-home/ project files that all other HomeMaster skills and agents build on. Use when the user says they want to start or plan a renovation, "nov projekt", "začni prenovo", or when my-home/ is missing.
---

# New HomeMaster project

Goal: create `my-home/` in the **current working directory** with an accurate picture of the home. Every later answer depends on it, so don't rush. Wrong facts here produce wrong instructions later.

## 0. Safety checks before writing
- If the current folder contains `.claude-plugin/` (it's the plugin repo itself), **stop** and tell the user to create a separate folder for their home, e.g. `MyHome/`. Their private data must not end up in the plugin repository.
- If `my-home/` already exists, don't overwrite it. Offer to update specific parts.

## 1. Interview
Ask in **small batches (3–5 questions)**, conversationally, in the user's language. Detect the language from their first message, and confirm it as question 1. Accept "don't know". Record it as unknown and say who could find out. Explain briefly *why* you ask when it's not obvious.

**Batch A: basics**
1. Language for all answers (e.g. Slovenian / English)
2. Country (drives regulations: see the knowledge skill's `regions/`)
3. Property type: house / flat in an apartment block / cottage / other
4. Year built and any earlier renovations (age → asbestos risk, old wiring, old pipes)
5. Construction: brick, concrete, wood frame, stone, unknown? Floor structure: concrete slab or wooden joists? (Wooden floors change waterproofing and tiling a lot.)

**Batch B: scope**
6. Which rooms and areas will be renovated, and in what order? Which one first? Offer the room types: bathroom (and WC), kitchen, living room, bedroom, hallway/entrance, basement, outdoor stairs, terrace/balcony, wellness (sauna, steam, hot tub), roof and attic, facade, garden structures (shed, pergola, carport, fence, retaining wall), pool (outdoor or indoor), indoor stairs, chimney and stove, garden and landscaping, irrigation, smart home (a layer over the whole house), or **other** (office, utility, garage, attic, ...). Ask also about the whole home: floors/levels, whether windows, insulation, heating, the panel or the roof are in scope.
7. Do you live there during the works? (→ a second working bathroom, dust protection)
8. Timeline / deadline, and the season the work will happen in (→ curing temperatures)
9. Budget: total and/or per room, and whether it's firm

**Batch C: you**
10. Experience per trade, on a 0–3 scale: demolition, plumbing, electrical, drywall, screed, waterproofing, tiling, painting
11. Physical limits or help available (heavy lifting, large-format tiles need 2 people)
12. Tools you already own (list them roughly; we'll refine per task)

**Batch D: the first room** (repeat for every room later). Load the knowledge skill's `references/rooms/<type>.md` for that room type, and ask its **Extra interview questions** in addition to the common ones below.
13. Dimensions: length × width × height, door and window positions and sizes. A sketch photo or rough plan helps.
14. Current state: what's there now, what stays, what goes
15. Wishes: function, style and key choices for this kind of room (e.g. bathroom: shower or bath, wall-hung WC, underfloor heating, tile format; kitchen: layout and appliances; bedroom: wardrobes and sleeping needs), storage
16. Known problems: damp, mould, cracks, slow drains, weak water pressure, tripping breakers

## 2. Create the files
Copy the templates from this skill's `templates/` folder and fill them with the answers:

| Template | Creates |
|---|---|
| `templates/profile.md` | `my-home/profile.md` |
| `templates/room.md` | `my-home/rooms/<room-slug>.md` (one per room mentioned; fill the first room fully) |
| `templates/tools.md` | `my-home/tools.md` |
| `templates/decisions.md` | `my-home/decisions.md` |
| `templates/log.md` | `my-home/log.md` |
| `templates/project-CLAUDE.md` | `CLAUDE.md` in the project root (only if none exists; otherwise append its section) |

Use the user's language for the file contents. Keep the English headings, because agents rely on them.

## 2b. Plan the first room in small steps
After the files exist, offer to run `/homemaster:plan-room` for the first room. It lists the work **in order as small packages** (for a bathroom: drains, WC frame, shower drain, supply lines, hot water, tests, screed, waterproofing, tiling, WC, basin, shower, glass, ...). Then `/homemaster:next-step` gives **one package at a time**.

## 3. First review
After writing the files:
1. Load the `homemaster:knowledge` skill and run the **safety-reviewer** agent on the profile (age, construction, apartment block, electrical, asbestos).
2. Tell the user, briefly:
   - what you recorded (a short summary)
   - **the critical flags** from the safety review
   - the **unknowns that block planning** (e.g. floor structure, ceiling height, where the stack is)
   - the next step: plan the first room (once `/homemaster:plan-room` exists; until then, the **project-lead** agent)
