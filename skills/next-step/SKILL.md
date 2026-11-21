---
name: next-step
description: Give the user the instructions for ONE work package at a time (for example only "WC frame", or only "shower glass"), in the right order for their room, with a dependency check first. Use when the user asks "what is next", "kaj je naslednji korak", "navodila za WC element", "kako namestim steklo za tuš", or says they finished a step. Reads my-home/rooms/<room>-plan.md, delivers one short work card, updates the plan and the log.
---

# Next step: one work package at a time

The user wants instructions **in small pieces, in order**, not a whole room at once. This skill delivers **one work package** as a **work card** and keeps the plan and the log up to date.

## Inputs
- Optional: a package id or a name (for example `wc-frame`, "shower glass"). If missing, take the **first package in the room's plan that is `todo` or `doing` and whose `after` packages are done**.
- The room (ask only if there are several rooms and it is not clear).

## Procedure
1. Load the `homemaster:knowledge` skill. Read `my-home/rooms/<room>-plan.md`. **If there is no plan, run `/homemaster:plan-room` first.**
2. Read `references/packages.yaml` (and `sequences.yaml` for the room's order). Find the package: its `task`, `src` (the technique), `after`, `who`, `time`. If the package has a `part` (`rough-in` or `fit`), **use only that part** of the source section (the section has both, for example `Rough-in part` and `Fit part`).
3. **Pick the package** (see Inputs). If the user names a package that is **not yet allowed** (a prerequisite is not done), **say so, name the missing steps, and offer to do them first**. Don't just comply.
4. **Run the dependency check** for the package's graph `task` (the `dependency-checker` agent or the same steps): the `requires` against `log.md`, the room file and the decisions, plus the upstream waiting times. **Lead with blockers** (`critical`, not confirmed). If blocked, stop and say what to do first.
5. **Read the sources** in `src` (the file and the heading) and also the sections the **cross-trade** notes point to (for example `sanitary.md` for backing when you give the drywall step). Use the user's real dimensions, tools and decisions, and the **tool list** `tools.md` (have / buy / rent).
6. **Write the work card** (below) in the user's language. **Only this package.** Keep it to **about one page** (roughly 250–500 words). If the package is bigger, **split it** into two cards ("prepare" and "do") and give the first.
7. **Offer the next step**: name the next 2–3 packages in the plan and what they wait for. Ask whether the user is ready, or wants to log this one as done.
8. **When the user says it is done:** record it. Append to `my-home/log.md` (date, the package, products and classes used, measurements, photos) and set the package **`done`** in the plan. If it has a waiting time (screed, waterproofing, adhesive, silicone), set the **next packages to `waiting` with the earliest start date**. Then continue with step 1.

## The work card
```
## <Package name>  (<stage> · <room> · <who> · about <time>)

**Why now / what it depends on:** one or two lines (what must be done, what this unlocks)

**✅ Before you start:** checklist from the graph (✔ done / ✖ not done / ? unknown)
**🧰 Tools:** have / buy / rent (from tools.md)
**📦 Materials:** classes and quantities for this room (see quantities.md), with the math
**🔢 Steps:** 6–12 numbered steps, each with how, the check and the time
**💡 Tips:** 2–4 practical points
**❌ Mistakes to avoid:** 3–5
**⏱️ Waiting after:** drying or curing, with a date if the log has one
**🔍 Check:** how to verify (a level, a straightedge, a pressure test, dry paper, photographs)
**🔗 Other trades:** only what matters now (the step before and after, backing, photographs, levels)
**➡️ Next:** the next 2–3 packages
```
Use the section headings translated by the glossary (`glossary-<lang>.md`).

## Rules
- **One package per answer.** Never the whole room. Never the steps of later packages (only name them).
- **Order is binding.** Don't skip ahead unless the user says why and the checker agrees.
- **Safety and licensed work first:** if the package is `pro` or has a licensed part, say it at the top and give only the **preparation** the user may do. Never help bypass a legal requirement.
- **No brands**, exact numbers with units, product classes, data-sheet values over "typical".
- **Math shown** for quantities, rounded up to whole packs.
- **Ask before logging** anything as done. Never mark a step done from an assumption.
- **Photograph and measure:** every card that closes something in a wall or a floor ends with the photograph reminder.
