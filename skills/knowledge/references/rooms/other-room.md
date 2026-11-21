# Room type: other rooms (office, children's room, utility/laundry, garage, attic, ...)

Type id: `other`. Map the room to the closest room type, then add what is different.

| Your room | Start from | Add |
|---|---|---|
| Home office, guest room, children's room, dining room | `bedroom` or `living-room` | data cabling and lighting for work (≥ 500 lx), sound insulation, extra sockets. For children: safe sockets, window stops, durable paint |
| Utility room, laundry, WC with washing machine | `bathroom` (wet floor) or `kitchen` | floor drain or a drip tray, waterproofed floor, ventilation (dryer), a 3-phase or dedicated circuit, a stack close by |
| Garage or workshop | `basement` (moisture, floor) and `garden-structures` (if free-standing) | concrete floor, drain, dust extraction, 3-phase sockets, fire safety, vehicle loads |
| Attic conversion | `roof-attic`, then `bedroom` or `living-room` | roof insulation and vapour control (the most failure-prone), roof windows, headroom rules, stair, fire escape, structural check of the floor and the rafters, **permit**. See `roof-attic.md`. The roof work itself belongs to a roofer and a structural engineer |
| Staircase (indoors) | `indoor-stairs` (and `hallway` at its foot) | riser/tread consistency, handrail, lighting, impact sound |
| Balcony | `terrace` | structural load and waterproofing over living space, railing rules. Often shared property |
| Conservatory / winter garden | `living-room` + `windows-install` | solar overheating, ventilation, condensation, thermal separation from the house |

## Decide first
- Which type in the table is closest, and what is different (loads, wet floor, escape, permit)
- The floor build-up and the finished floor level, the heating, the electrical load and the ventilation
- What stays, what goes, who does what (you vs. a licensed professional)

## How to use
- Say in the project file which type you start from. The agent loads that room file, and this one for the differences.
- If the room is truly different, say so and the agent will build the sequence from the dependency graph. It will then say that room-specific knowledge is not in the knowledge base yet.

## Common mistakes
- Treating an attic or a garage conversion as a simple "paint and floor" job. Structure, insulation, fire and permits dominate.
- Underestimating the electrical load in utility and workshop rooms.
