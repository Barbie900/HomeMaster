---
name: plan-room
description: Build the ordered step-by-step plan for one room or area of the user's home, split into small work packages (for a bathroom for example drains, WC frame, shower drain, supply lines, hot water, tests, screed, waterproofing, tiling, WC, basin, shower, glass). Use when the user wants to start working on a room, asks "what do I do first", "in what order", "razdeli navodila na korake", "načrt za kopalnico/kuhinjo/...", or after /homemaster:new-project. Writes my-home/rooms/<room>-plan.md and does NOT give the full instructions, only the plan.
---

# Plan a room as ordered work packages

A renovation instruction for a whole room is too big to follow. This skill turns a room into **a short ordered list of small work packages**. The user then does one package at a time with `/homemaster:next-step`.

## Before you start
1. Load the `homemaster:knowledge` skill. Read `references/packages.yaml` (the packages) and `references/sequences.yaml` (the order per room type), `references/dependencies.yaml` and `references/trades/planning.md`.
2. Read `my-home/profile.md`, the room file `my-home/rooms/<room>.md` (its `Type:` line selects the room sequence), `decisions.md`, `tools.md` and `log.md`.
3. If `my-home/` or the room file is missing, run `/homemaster:new-project` first (or ask the key facts: type, size, what exists, what is planned).

## Steps
1. **Take the room's sequence** from `sequences.yaml` (the list for the room's `Type:`) and the package details from `packages.yaml`.
2. **Ask only the questions that decide optional packages** (those with `opt: true`), in one short batch, with a recommendation for each. Examples for a bathroom: tiled walk-in shower or tray and a **glass screen**? Bath too? **Underfloor heating?** Radiator or towel rail? **New hot-water appliance** or the existing one? Screed to be poured or the existing one kept? Smart-home cabling? **Remove** the packages that do not apply. Do not ask what the room file or the profile already say.
3. **Check the order** (`after:`). Keep the sequence order. If you removed a package that others depend on, keep the dependants' real prerequisites in mind and tell the user.
4. **Add dates and waiting times.** From `log.md` mark packages already done. For the rest, take the **waiting times** from the graph (`wait_after`) and the package `time`, and write **earliest start** where the log has dates. Make the waits visible as their own lines (for example "screed drying: about 6–8 weeks, measure CM").
5. **Mark who does what:** `diy`, `diy+pro` (the licensed part named) or `pro`. Put **licensed work and bookings with lead times** in a short list at the top (electrician measurements, gas, chimney sweep, engineer, glass maker).
6. **Mark parallel work:** things that can be done while something dries or is delivered.
7. **Write `my-home/rooms/<room>-plan.md`** in the user's language, with this layout:

```
# Plan: <room>  (type: <type>)
Created: <date>   Next up: <package>   Home context: <one line>

## Book and order first
- <licensed work, long-lead items, with lead times>

## Steps in order
| # | Stage | Package | Who | Time | Waits for | Status | Earliest start |
|---|-------|---------|-----|------|-----------|--------|----------------|
| 1 | Decide | Survey and measure | you | 2–4 h | | todo | |
...

## Parallel while waiting
- ...

## Decisions that change the plan
- ...
```
   Status values: `todo`, `doing`, `done`, `waiting`, `blocked`, `skipped`. Use the package names in the user's language (`name.sl` or `name.en`) and keep the package ids in a short column or in brackets so the next skill can find them.
8. **Run the dependency checker** (agent `dependency-checker`) for the **first three packages** that are not done and report blockers.
9. **Tell the user, briefly:** how many steps, the first step, the **critical decisions to make now** (finished floor level, shower type, tile format, appliance models), and **what to book first**. **Do not** write the instructions of the steps here.

## Rules
- **Never put the whole room's instructions in the plan.** The plan lists packages only. The detail comes one package at a time (`/homemaster:next-step`).
- **Respect the order** and say why a step is where it is when it is not obvious (for example "the glass is ordered after the tiles, from the finished walls").
- **Licensed-only work** (gas, the panel, electrical connection and measurements, the chimney sweep's sign-off, structural changes) is its own step and is marked `pro`.
- **Do not invent facts** about the room: ask or mark "unknown".
- Keep the plan **short enough to read in two minutes**.
