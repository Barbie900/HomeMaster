# Room type: smart home (whole-house system)

Type id: `smart-home`. Not a room but a **layer over the whole house**: network, control, sensors and energy.

## What makes it different
- **Cabling is decided during the rough-in** of every room. After plaster it's expensive.
- **A standard and a hub** are house-wide decisions.
- **Mains-voltage devices and the panel** are licensed work. **Network and sensors** are DIY.
- **Security and privacy** are part of the job (network, cameras, cloud).
- **Safety functions must work without the internet.**

## Decide first
- Goals and what must work without the internet (lights, heating, alarms, locks)
- System standard (wired bus, wireless mesh with a local hub, Matter, Wi-Fi cloud) and long-term support
- Network cabling plan (every room, ceiling access points, a switch cabinet and a UPS)
- Neutral wires at every switch box, spare conduits, power at blinds and sensors
- Who does what (you vs. the electrician) and the panel capacity (PV, battery, EV charger, heat pump)

## Task sequence (graph ids)
`survey-and-permits` → `smart-home-plan` → `panel-and-main-services` → `smart-home-cabling` (during `electrical-rough-in`) → `electrical-rough-in` → `wall-plaster-repair` → `electrical-fit-out` (licensed) → `smart-home-commission`

## Room-specific rules and numbers
See `trades/smart-home.md`.
- Cat 6 or Cat 6a to every room (fixed cable up to 90 m), two outlets in living rooms, wired ceiling access points (≈ one per 60–100 m² and per floor).
- Neutral at every switch box, boxes ≥ 60 mm deep, spare conduits Ø25–32 mm.
- Low-voltage cables apart from mains (≥ 5–10 cm or separate conduits), labelled at both ends, photographed.
- Separate networks for devices and guests, updates on, no default passwords, no open ports.

## Extra interview questions
- What do you want it to do (lights, heating, blinds, security, energy, irrigation, pool)?
- Do you rent or own? New wiring possible (open walls) or retrofit?
- Who lives here (children, elderly, guests)? Who will maintain it?
- Existing router, TV, NAS, cameras? Internet speed and provider?
- PV, battery, EV charger, heat pump planned?

## Common mistakes
- No neutral in switch boxes, no network cable to the ceiling and outdoors.
- Cloud-only devices and many apps.
- Safety functions that depend on the internet.
- One flat network with default passwords.
- No manual switches left.

## Links to other rooms
- All rooms (cabling in the rough-in), garden and irrigation, pool, wellness, kitchen (appliances), bedroom and living room (scenes, blinds), windows (shading).
