# Trade: Smart home (network, control, sensors, energy)

Graph tasks: `smart-home-plan`, `smart-home-cabling`, `smart-home-commission`. Typical values: the **device makers' installation sheets**, the **electrical rules** and **data-protection law** win.

**DIY level:** **low-voltage** work is DIY: network cabling, bus and sensor cables, conduits, hubs, access points, battery or plug-in devices, configuration, security, automation logic. **Mains-voltage** devices (smart switches and dimmers in the wall, relays in the panel, blinds motors wired to mains, EV charger, heat pump controls, PV and battery) and **anything in the electrical panel** are **licensed electrician** work in most countries. **Smoke and CO alarms and door locks must work without the internet.**

## Principles (what separates a good smart home from a frustrating one)
1. **Cabling is the foundation.** Wires last 30+ years, gadgets 5–10. **Pull network and conduits during the rough-in**, even if you install devices later.
2. **Local control first.** The home must work when the internet, the cloud or the vendor is gone. Prefer **local protocols** (wired bus, Zigbee, Z-Wave, Thread and Matter) and **a local hub**, and keep cloud as an extra.
3. **Every switch must still work by hand,** for guests, the family and a dead hub. A **manual fallback is part of the design.**
4. **Fewer, simpler automations** that people understand beat clever ones nobody trusts.
5. **Safety functions are independent** of the smart system (smoke and CO alarms, heating limits, door locks).
6. **Privacy and security by design:** no unneeded cameras or microphones, separate networks, updates, no default passwords.

## Choose the system (comparison)
| Approach | Pros | Cons | Fits |
|---|---|---|---|
| **Wired bus (e.g. KNX)** | very reliable, standard across brands, long life, local | needs planning, special cable, usually a programmer or integrator, costly | new builds, full renovations, strip-out to bare walls |
| **Wireless mesh (Zigbee, Z-Wave, Thread) with a local hub** | cheap, easy to add, many devices, batteries | radio range, mesh planning, hub is a single point | **most renovations**: retrofits without new cables |
| **Matter over Thread or Wi-Fi** | a common standard across brands, local | still maturing, device support varies | new devices, mixed ecosystems |
| **Wi-Fi cloud devices (per brand apps)** | simplest start | cloud dependence, many apps, weak security, break when the vendor drops support | gadgets, not the core |
**Recommendation:** **structured network cabling to every room and conduits + neutral wires everywhere (for a fully renovated home), then a local hub with Zigbee/Thread and Matter devices for flexibility.** Choose **KNX** only if you want a fully wired, installer-supported system and have the budget.

## Planning (task: `smart-home-plan`)
- **List the goals and rooms:** lighting scenes, heating zones (thermostats per room, `heating.md`), blinds and shading, security (door and window contacts, cameras, alarms), **safety sensors** (smoke, CO, water leak sensors at the washing machine, boiler and bathrooms), energy monitoring, **irrigation** (`irrigation.md`), **pool** controls, entertainment.
- **Network:** a **switch cabinet** (structured cabling) with a patch panel, a PoE switch and a UPS (small battery backup). **Cat 6 or Cat 6a** (fixed cable up to 90 m) to **every room (two or more outlets in living rooms), the ceilings (access points, cameras), outdoor positions, the TV spots and the garage**. **Wi-Fi access points on the ceilings** (one per ≈ 60–100 m² and per floor, wired back), **not one router in a corner**.
- **At every switch box:** a **neutral wire** (so smart switches and sensors work), and ideally **a 3-core or 5-core cable** and a **deep box** (≥ 60 mm). **Spare conduits** (Ø25–32 mm) between floors and to the attic and the cellar.
- **Blinds and shading:** power at each window (230 V or low-voltage motors), and the **control cable** for a wired system.
- **Outdoors:** conduits to lights, cameras, the gate, irrigation, a weather station and the pool. **Outdoor power by a licensed electrician.**
- **Energy:** **panel capacity** (`panel-and-main-services`), a **PV and battery system** (a professional installation and a grid-operator notification), an **EV charger** (a licensed installer, load management), a **heat pump** and its smart-grid readiness.
- **Documentation:** a floor plan of every cable and device, labelled ports, and **an owner's manual** for the household.

## Cabling (task: `smart-home-cabling`)
1. **Mark the routes** on the plan. **Keep low-voltage cables apart from mains cables** (typically ≥ 5–10 cm or in separate conduits, cross at 90°) to avoid interference.
2. **Pull the network cables** (home-run star topology: every outlet back to the cabinet), **leave 2–3 m of slack** at each end, **label both ends** with the same ID, and **don't kink or over-tighten cable ties.**
3. **Conduit with pull-cords** to windows, the garden, the garage and the loft.
4. **Keep neutral wires** at every switch box and **boxes deep enough** for the devices.
5. **Photograph everything** with a tape measure before plaster, and record the IDs.
6. **Test:** a cable tester for each run (continuity and wire map), and later a network certifier or a speed test.
7. **Terminate** the ends in the cabinet with a punch-down tool (patch panel) and at the room end with keystone jacks (**the same wiring standard on both ends**).

## Commissioning and security (task: `smart-home-commission`)
- **Mains devices and panel work by the electrician.** Test the **RCDs** and the devices.
- **Network security:** change all default passwords, **a strong unique password per device and account**, **two-factor login**, **automatic updates**, **separate networks (VLANs or at least a guest and an "IoT" network)** so a cheap camera can't reach your laptop, **no ports opened to the internet** (use a VPN for remote access), a **router with current firmware**.
- **Backups** of the hub and controller configuration, **an offline copy of the plan and the logins** in a safe place.
- **Safety:** smoke and CO alarms **not dependent on the cloud**, **leak sensors** with local sirens (and optionally a **water shut-off valve**), **heating limits** in hardware thermostats.
- **Privacy:** cameras only where needed and not into neighbours' property, **voice assistants** muted or placed with care, data minimisation, **GDPR** where applicable. **Tell visitors** about cameras.
- **Handover:** a one-page guide, **the manual fallback at every switch**, and a **maintenance routine** (battery changes, updates, annual test of alarms).

## Useful automations (start small)
- **Lighting:** presence sensors in hallways, bathrooms and stairs, scenes in living rooms.
- **Heating:** per-room schedules and a **window-open** setback, **a presence setback**.
- **Blinds:** sun and temperature-based shading (cuts summer overheating).
- **Leak and smoke alerts** to your phone and a siren.
- **Irrigation:** weather-based and soil-moisture-based.
- **Energy:** run the washing machine, the heat pump and the EV charger when the sun shines or the tariff is low.

## Tools
Cable tester, **punch-down tool**, **crimp tool** (only if you terminate plugs), **fish tape**, **conduit spring**, drill and long bits, label printer, cable ties and Velcro, a laptop, **a multimeter and a voltage tester** (always check that mains is off before touching switch boxes, and have the electrician do the connection), a tablet for the plan.

## Common mistakes
- **No neutral** in switch boxes, so smart switches don't fit.
- **No network cable** to the ceiling and outdoor positions.
- **Cloud-only devices** that stop working when the app is closed.
- **Everything on one network** with default passwords.
- **Safety functions** depending on the app.
- **Too many different standards** and apps.
- **No manual switches** left for the family and guests.
- **Mains and data cables together** in the same conduit.

## Quality checks
- Every run passes the tester, all labels match the plan, **the house works with the internet unplugged**, alarms trigger locally, and the family can operate the lights without the app.

## Cross-trade
- Electrical rough-in (`electrical.md`: the neutral, boxes, panel, circuits), heating (thermostats), windows and blinds, irrigation, pool, kitchen and appliances, wellness, security, data protection, and the region file.

## Element: network cabinet and structured cabling
1. **Cabinet** (a wall cabinet or a niche) **central, ventilated, with power (two sockets), a UPS space**, **≥ 60–80 cm clear in front**.
2. **Cabling:** **Cat 6 or Cat 6a** from **every outlet back to the cabinet** (star topology), **≤ 90 m**, **slack 2–3 m at both ends**, **labelled at both ends**, **no kinks, loose cable ties**.
3. **Terminate** on a **patch panel (punch-down) and keystone jacks**, **the same wiring standard (T568B) at both ends**.
4. **Test** every run with a **cable tester** (wire map and continuity), **photograph** the routes.
5. **Keep** the low-voltage cables **≥ 5–10 cm** from mains or in **separate conduits**, **cross at 90°**.

## Element: Wi-Fi access points
1. **Ceiling-mounted access points** wired back (**PoE**), **one per ≈ 60–100 m² and per floor**, **clear of metal**, **centrally in rooms**.
2. **Channel plan** per the equipment, **separate SSIDs** (main, guests, devices).
3. **Test** with a **survey app** after the walls are finished.

## Element: lighting control
1. **Choose:** **smart switches or dimmers** in the wall (**mains-voltage devices by the electrician**), **smart bulbs** (cloud-dependent), or **a wired bus**.
2. **A neutral** in every switch box. **Wall switches must work without the app.**
3. **Scenes** (evening, cinema, night), **presence sensors** in halls, bathrooms and stairs.
4. **Test** the manual operation and the offline behaviour.

## Element: heating and room thermostats
1. **Thermostat per room** (or per zone), **sensors in the right place** (not near a stove or in sun), **valve actuators** on UFH manifolds.
2. **Schedules, a window-open setback and a presence setback**, **a weather-compensated flow temperature**.
3. **Hardware limits** (floor temperature, boiler) **independent of the app**.

## Element: blinds and shading
1. **Motors** (230 V by the electrician, 24 V or battery models), **wind and sun sensors**, **a manual override**.
2. **Rules:** **sun-based shading** in summer, **open on cold sunny winter days**.
3. **Safety:** **no cords** within reach of children.

## Element: sensors and alarms
1. **Smoke, CO and water-leak sensors** (**local sirens**, **not dependent on the cloud**), **leak sensors** at the washing machine, boiler and bathrooms, optionally **a water shut-off valve**.
2. **Door and window contacts, motion sensors** (privacy: **not in bedrooms or bathrooms if the data leave the house**).
3. **Test** monthly, **batteries** yearly.

## Element: cameras and access
1. **Only where needed**, **on your own plot**, **not filming neighbours or public space**, **local recording where possible**, **signage** if required.
2. **Locks:** a **smart lock with a key backup**, **a mechanical override**, **no single point of failure**.
3. **Network:** **separate VLAN**, **no open ports**, **updates on**.

## Element: energy, PV and EV charging (planning)
1. **PV, battery, EV charger and heat pump** are **licensed installations** (and often **the grid operator's approval**). **You plan:** the **load list**, **the roof or wall area**, **the panel capacity**, **conduits** (to the roof, the garage, the cabinet), **a space for the inverter and battery** (fire and ventilation rules).
2. **Energy monitoring:** **a smart meter or a clamp-based monitor**, **a dashboard**.
3. **Load management** so the **EV charger and the heat pump don't overload the connection**.
