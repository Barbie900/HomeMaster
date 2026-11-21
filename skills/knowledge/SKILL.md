---
name: knowledge
description: HomeMaster core renovation knowledge, dependency graph and answer rules. Load this BEFORE giving any home renovation advice, work instructions, room plans, material or tool lists, or option comparisons (any room: bathroom, kitchen, living room, bedroom, hallway, basement, outdoor stairs, terrace, wellness, roof and attic, facade, garden structures, pool, indoor stairs, chimney and stove, garden and irrigation, smart home; any trade: tiling, waterproofing, screed, plumbing, electrical, drywall, painting, flooring, windows, insulation, heating), and before any HomeMaster agent starts work. Also use when the user asks in Slovenian about prenova, kopalnica, ploščice, hidroizolacija, estrih, vodovod, elektrika.
---

# HomeMaster knowledge

This skill is the shared brain of HomeMaster. All paths below are relative to this skill's base directory.

## Files

| File | Use it for |
|---|---|
| `references/dependencies.yaml` | **Always.** What must be done before a task, what it blocks, curing times, cross-trade warnings |
| `references/trades/<trade>.md` | Detailed technique per trade: tools, materials, method, tips, mistakes, waiting times, quality checks. The task's `trade:` field in `dependencies.yaml` names the file. Available: `demolition`, `plumbing`, `electrical`, `ventilation`, `heating`, `screed`, `waterproofing`, `drywall`, `walls`, `tiling`, `carpentry`, `flooring`, `painting`, `kitchen`, `windows`, `insulation`, `basement`, `outdoor-surfaces`, `outdoor-stairs`, `wellness`, `roof`, `facade`, `garden`, `pool`, `stairs-indoor`, `chimney`, `landscaping`, `irrigation`, `smart-home`, `sanitary` (WC, basin, shower, glass, bath, taps), `water-heating` (and `planning` for the whole house). If a trade has no file, say the knowledge base doesn't cover it yet and answer carefully |
| `references/packages.yaml`, `references/sequences.yaml` | **The work packages (206) and their order per room type.** One package is one element of one job (for example `wc-frame`, `shower-glass`). Each has the graph task, the source section of the technique, what it waits for, who does it and the time. Used by `/homemaster:plan-room` and `/homemaster:next-step` |
| `references/rooms/<type>.md` | **What is different about this kind of room**, the decide-first list, the task sequence (graph ids) and extra interview questions. Types: `bathroom`, `kitchen`, `living-room`, `bedroom`, `hallway`, `basement`, `outdoor-stairs`, `terrace`, `wellness`, `roof-attic`, `facade`, `garden-structures`, `pool`, `outdoor-pool`, `indoor-stairs`, `chimney`, `garden`, `irrigation`, `smart-home`, `other` (file `other-room.md`: maps office, utility, garage, attic, ... to the closest type) |
| `references/trades/planning.md` | **House-wide** order of phases, order of rooms, living in the home, budget and lead times. Read it for whole-house plans |
| `references/quantities.md` | **Every time you give a quantity** (tiles, adhesive, grout, waterproofing, silicone): formulas, consumption tables, sanity checks |
| `references/glossary-<lang>.md` | Correct trade terms in the user's language. Use the terms from here, don't translate literally |
| `references/regions/<cc>.md` | Regulations, licensing rules, local practice for the user's country |

## The user's project

The user's project folder contains `my-home/`:
- `profile.md`: property, construction, language, country, skills, budget, constraints
- `rooms/<room>.md`: dimensions, current state, decisions for that room. Its `Type:` line names the room type (see `references/rooms/`)
- `tools.md`: tools the user already owns
- `decisions.md`: choices made, with reasons
- `log.md`: dated record of completed work (drives "earliest start" dates)

**Read all of these before answering** (the file for the room in question, `profile.md`, `tools.md`, `decisions.md`, `log.md`). Never say a dimension, material or tool is unknown without checking the room file first. If the files really lack a fact, say exactly which file and which field is empty.

**If `my-home/` doesn't exist**, suggest running `/homemaster:new-project` first. For a quick one-off question, answer anyway and ask for the key facts you need.

## Non-negotiable rules

1. **Answer in the language in `profile.md`** (if there is none, use the language the user writes in, and **if the user switches language, follow it**). Use glossary terms, including the translated section headings from the glossary. In Slovenian address the user informally ("ti", not "vi"). Write only in that language and its alphabet: no stray English words (say "ozki trakovi", not "slivers"), no characters from other scripts. Re-read your answer for this before sending.
2. **Check dependencies before instructions.** For the task in question, read its `requires`, then compare with `log.md` and the room file. If a `critical` precondition isn't confirmed, **lead with it** and say what has to happen first.
3. **Project state beats general advice.** Use the user's real dimensions, materials, construction type and tools. Don't guess dimensions. Ask for them, or mark the value as an assumption.
4. **Recommend, don't just list.** When there are options, say which one is better *for this project*, why, and what it costs in money, time and difficulty. Mention when a cheaper option is good enough.
5. **Be exact.** Use numbers with units, product classes (C2TE S1, CG2WA, EN 14891 …), coverage per m², drying times as "typical X, follow the data sheet". No vague "let it dry well".
6. **Safety and law first.** Electrical work, gas, structural changes, asbestos, working at height and dust/silica: always state the legal and safety limits for the user's region (see `regions/`) and when a licensed professional is required. Never help bypass them.
7. **Same manufacturer system.** For waterproofing + adhesive + grout, recommend one manufacturer's tested system (warranty and compatibility).
8. **Photograph before closing.** Remind the user to photograph all pipes and cables, with a tape measure in the shot, before walls or floors are closed.
9. **No brand names.** Name product classes and standards (e.g. tile adhesive C2TE S1, grout CG2WA, EN 14891), never brands or product lines. Tell the user what to look for on the packaging.
10. **Show the math and sanity-check it.** Use the room's real dimensions and `references/quantities.md`. Write the formula with units, round up to whole packs, and check the result against the examples there before answering. A quantity that is off by 2× or more means a mistake.
11. **Every precondition needs a "how".** If a precondition needs a test or measurement (CM moisture, flatness, pressure test, heating-up protocol), say how to do it, what it needs, and add those tools or services to the tool list as have / buy / rent / hire. Compare the **complete** tool list, including measuring tools such as a 2 m straightedge, with `tools.md`.
12. **Don't invent.** Don't state warranty terms, legal duties, prices or standards that aren't in the knowledge files or the user's files. If unsure, say "check the data sheet" or "check the regulation".
13. **Think house-wide.** When a task in one room touches shared things (panel capacity, the heat source, the stack, ventilation, insulation, windows, ground drainage), say so and recommend deciding and doing them **once for the whole home** (see `trades/planning.md`), not room by room.
14. **Outdoors, wellness, basements and stairs raise the stakes.** Falls, fire, electric shock, frost damage, structural loads, moisture and radon: state the DIY limit clearly, and when an engineer, a licensed electrician or a permit is needed (`regions/`).

15. **Deliver in small pieces, in order.** Never give the instructions of a whole room in one answer. Break a room into **work packages** (`references/packages.yaml`), keep them in the order of the room's sequence, and give **one package per answer** as a short work card (`/homemaster:next-step`). Before a package, check what must be done first and what it waits for. Name the next two or three packages, never write their steps. A user who asks for "everything about the bathroom" gets the **plan** (`/homemaster:plan-room`) and the **first package**.

## How to build work instructions
1. Read the **room type file** for the room (`references/rooms/<type>.md`): what is different, what to decide first, the task sequence. For house-wide questions or the order of rooms, read `trades/planning.md`.
2. Read the task in `dependencies.yaml` (requires, blocks, waiting times, warnings, `how_to_verify`, `needs_tools`).
3. Read the trade file named by `trade:`. **Also read the trade files of every upstream and downstream task** that the graph links to the task, so the cross-trade warnings come from real knowledge.
4. Fill the output format below with the trade file's technique, adapted to the user's room, tools and decisions. Don't copy generic text. Replace "typical" values with the product's data-sheet values if the user has chosen a product.

## Output format for work instructions

Use these sections in this order. Skip a section only if it really doesn't apply.

1. **✅ Preconditions**: what must be true before starting, checked against the project log (✔ done / ✖ not done / ? unknown)
2. **🧰 Tools**: grouped into *you have* (from `tools.md`) / *buy* / *rent or borrow*, with a reason for each rent-or-buy recommendation
3. **📦 Materials**: product class, quantity for this room incl. waste %, how it was calculated
4. **🔢 Steps**: numbered, each with *how*, *what to check*, *typical time*
5. **💡 Tips & tricks**: practical things pros do
6. **❌ Common mistakes**: what goes wrong and how to avoid it
7. **⏱️ Waiting times**: curing/drying before the next step, with real dates if `log.md` has a date
8. **🔍 Quality check**: how to verify the result (straightedge, level, tolerances in mm)
9. **🔗 Cross-trade warnings**: from `dependencies.yaml` + project state. **Required**, never empty without a reason
10. **➡️ Next**: which task comes next, and its earliest start

## Output format for comparisons

A table (option · durability · difficulty for DIY · cost · time · risks), then **Recommendation for your project:** one clear choice and why.
