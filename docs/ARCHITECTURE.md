# Architecture

HomeMaster has four layers. Knowledge only connects when that is designed in, and the dependency graph is how it is designed in.

```
┌──────────────────────────────────────────────────────────────┐
│  SKILLS (workflows the user runs)                            │
│  new-project · plan-room · instructions · compare · shopping │
└───────────────┬──────────────────────────────────────────────┘
                │ orchestrate (main thread)
┌───────────────▼──────────────────────────────────────────────┐
│  AGENTS (specialists, run as subagents)                      │
│  project-lead · dependency-checker · safety-reviewer         │
│  + trade specialists (tiler, plumber, electrician, …)        │
└───────────────┬──────────────────────────────────────────────┘
                │ all read
┌───────────────▼───────────────────┐  ┌───────────────────────┐
│  KNOWLEDGE (plugin, shared)       │  │  PROJECT (user folder)│
│  skills/knowledge/                │  │  my-home/             │
│   SKILL.md   principles + format  │  │   profile.md          │
│   references/dependencies.yaml ⭐ │  │   rooms/<room>.md     │
│   references/trades/*.md          │  │   tools.md            │
│   references/glossary-*.md        │  │   decisions.md        │
│   references/regions/*.md         │  │   log.md              │
└───────────────────────────────────┘  └───────────────────────┘
```

## Why the knowledge lives in a skill

Plugin agents and skills can't rely on an absolute path to the plugin folder. A skill gets its base directory when it loads, so bundling the knowledge as `skills/knowledge/references/` makes it reachable from any project folder. Every agent loads `homemaster:knowledge` first.

## Rooms, trades and the graph

Three kinds of knowledge files work together:
- `references/dependencies.yaml`: **generic tasks** (what must be true before, what it blocks, waiting times, warnings). The same task serves many rooms: `floor-tiling` is used in a bathroom, a hallway, a kitchen and a terrace.
- `references/trades/<trade>.md`: **how to do the work** (tools, method, tips, mistakes, quality checks). The task's `trade:` names the file.
- `references/rooms/<type>.md`: **what is different about this room type**, what to decide first, the **task sequence** of the room (graph ids), the extra interview questions.
- `references/trades/planning.md`: **house-wide** order of phases and rooms.

A room file in the user's `my-home/rooms/` has a `Type:` line that selects the room-type file. The agents read the room type, then the graph tasks in its sequence, then the trade files.

## Work packages: instructions in small pieces, in order

A whole room's instructions are too long to follow. `references/packages.yaml` cuts every room into **work packages** (one element of one job: `wc-frame`, `shower-drain-body`, `shower-glass`, ...). It has two parts:
- `packages:`: each package has the graph `task` (preconditions), `src` (the section of a trade file that holds the technique), `after` (what must be done first), `who` (diy, diy+pro, pro), `time` and `opt` (may not apply).
- `sequences.yaml`: for every room type, the **ordered list** of packages (bathroom 45 steps, kitchen 47, living room 49, bedroom 43, hallway 43, basement 38, roof and attic 32, wellness 24, facade 21, garden 20, smart home 18, and so on).
- Each package points to **one element section** (`## Element: ...`) of a trade file. Sections with a rough-in and a fit part are marked with `part:`.

Skills use it:
- `/homemaster:plan-room` turns a room into `my-home/rooms/<room>-plan.md`: the ordered table, waiting times, who does what, what to book first.
- `/homemaster:next-step` gives **one package** as a short work card, after a dependency check, and updates the plan and the log.

A validation script checks that every package's task and source section exist, every sequence is in a valid order (each package after all of its `after` packages) and every room type has a sequence.

## The dependency graph (`dependencies.yaml`)

Each task declares:

| Field | Meaning |
|---|---|
| `name` | Display names per language |
| `trade` | Which trade knowledge file covers it |
| `requires` | Checks that must be true **before starting**, each with a `severity` and a `why` |
| `blocks` | Tasks that can't start until this one is done (and cured) |
| `wait_after` | Curing/drying before the blocked tasks may start |
| `how_to_verify` | How to perform a required measurement or test (optional) |
| `needs_tools` | Tools/services the task or its checks need. Agents add them to the tool list |
| `warnings` | Cross-trade pitfalls, optionally conditional (`if:` refers to profile/room facts) |

Severities:
- `critical`: do not start. Risk of failure, water damage, injury or legal issues
- `important`: quality or cost risk
- `tip`: good practice

`reference_lines` holds facts that many tasks share (e.g. finished floor level). This is where most expensive DIY mistakes come from.

## The project folder

Created by `/homemaster:new-project` in the user's own folder, not in the plugin. It also writes a `CLAUDE.md` there, so every session in that folder knows it is a HomeMaster project and which language to answer in.

`log.md` is what makes advice time-aware. Entries are dated, and the dependency checker computes the earliest start for downstream tasks from `wait_after`.

## Answer contract

Every instruction set follows the same sections (defined in `skills/knowledge/SKILL.md`). Its last section, **Cross-trade warnings**, is required and comes from the dependency graph plus the project state.
