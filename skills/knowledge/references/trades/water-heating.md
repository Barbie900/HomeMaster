# Trade: Water heating (domestic hot water)

Graph tasks: `water-heating-plan`, `water-heating-install`. Typical values: the **appliance's installation sheet**, your country's **drinking-water, pressure-equipment, gas and electrical rules**, and the installer's sign-off win.

**DIY level:** **planning and choosing** are yours. **Pipe work** at the appliance is DIY for a careful person. **Not DIY in most countries:** gas appliances, a **pressurised (unvented) cylinder** in some countries, the **heat source connection**, and every **electrical connection** (a licensed electrician). **Safety valves must never be blocked.**

## Options (comparison)
| Option | How it works | Pros | Cons | Fits |
|---|---|---|---|---|
| **Central source + cylinder (boiler or heat pump, 150–300 l)** | the heating system heats the cylinder | efficient, many taps, any number of bathrooms | space, standby losses, needs the heating system | whole-house renovation |
| **Heat-pump water heater (integrated, 200–300 l)** | an air-source heat pump on the tank | very efficient (≈ 3× the electricity use) | needs air volume and a drain, noise | all-electric homes |
| **Electric storage heater (5–200 l)** | an electric element in an insulated tank | simple, one point or a few | standby losses, wait to heat | small bathrooms, a kitchen |
| **Instantaneous electric** | an element heats the water as it flows | no tank, no standby loss | very high power (up to 18–27 kW, usually 3-phase) | a remote tap, low-demand points |
| **Gas instantaneous or combi** | a gas burner | good output | gas installer, flue | gas homes |
| **Solar thermal + cylinder** | collectors on the roof | free heat in summer | cost, roof work | with a central cylinder |
**Recommendation:** for a full renovation with a **heat pump or a boiler**: a **central cylinder** with a **circulation loop** if the bathrooms are far away. For a **single remote bathroom or a kitchen**: a **small electric storage heater** or a **low-power instantaneous unit at the basin**. Avoid a **27 kW shower heater** unless the panel can carry it.

## Sizing
- **Demand:** typically **30–50 l of 60 °C water per person per day** (≈ 40 l). A family of four needs **≈ 150–250 l storage** (with a heat pump or a fast reheat, less).
- **Instantaneous power:** **P (kW) ≈ 0.07 × flow (l/min) × temperature rise (K)**. Example: a shower of **8 l/min** with water heated **from 10 °C to 38 °C** (rise 28 K) needs ≈ **15.7 kW**, so an **18 kW (3-phase)** unit. **Check the panel and cable capacity** (`panel-and-main-services`).
- **Pressure and flow:** typically 2–4 bar. A **pressure reducer** if the mains pressure exceeds the appliance's rating (usually > 5 bar).
- **Location:** frost-free, **accessible**, **close to the tap that uses the most** (short pipes = faster hot water and less loss). **A 200 l full tank weighs ≈ 250 kg** (check the floor), and it needs a **floor drain or a drip tray**.

## Hygiene and safety (the part not to skip)
- **Legionella:** store hot water at **≥ 60 °C**, circulation return at **≥ 55 °C**, **no dead legs** (pipes with more than ≈ 3 l between the loop and the tap), **no stagnant lukewarm water** (25–45 °C). Flush taps that are rarely used.
- **Scalding:** a **thermostatic mixing valve** at the tap or the cylinder outlet, **≤ 43 °C** at showers and baths (lower for children and the elderly).
- **Safety group:** for a **closed (pressurised) tank**: a **safety valve** (rated pressure ≈ 6–10 bar, **never plugged or throttled**), a **non-return valve**, an **expansion vessel** (so the safety valve doesn't drip at every heating), and a **visible discharge pipe to a drain**.
- **Corrosion and scale:** an enamelled tank has a **magnesium anode** (check every 1–2 years). **Hard water** needs descaling or a softener. **Isolation valves and a drain** for service.
- **Electric:** a **dedicated circuit**, **RCD protection** and a **thermal cut-out** (by the electrician). **Never** run an element dry.

## Planning (task: `water-heating-plan`)
1. **List the hot-water points** (bathroom, kitchen, utility, any outdoor shower) and the distances from the source.
2. **Choose the system** (above) with the heat source decision (`heating.md`, `panel-and-main-services`).
3. **Size** storage or power. **Decide the location** and the access and the drain.
4. **Plan the circulation:** a loop with a pump and timer when the **farthest tap is > ≈ 7 m away or holds more than ≈ 3 l** in the pipe. **Insulate** the hot and the return lines.
5. **Plan the pipework** in the rough-in: hot and cold lines to every fixture, **isolation valves**, **the mixing valve**, and **pressure test** before closing.
6. **Electric and flue needs:** the **circuit**, **gas supply or flue** (licensed).

## Installation (task: `water-heating-install`)
1. **Mount the appliance** on a wall or floor rated for its weight, level, with the **clearances** the maker states.
2. **Cold supply:** isolation valve, **pressure reducer if needed**, **non-return valve**, **safety group** (closed tank) with the **discharge pipe** (≥ the valve's outlet size, falling, visible, to a drain). **Never** valve off the safety valve.
3. **Hot outlet:** the **thermostatic mixing valve** if used, **insulated pipes**, **the circulation return** if there is one.
4. **Expansion vessel** on the cold side (closed system) as the maker says.
5. **Fill the tank** with the vent open until air is out, **check every joint** for leaks, **pressure test** the pipes.
6. **Electrical connection** by the **licensed electrician**: dedicated circuit, RCD, **thermostat setting** (≥ 60 °C for storage, with a mixing valve at the taps).
7. **Commission:** heat up, **check the temperature at the taps** (a thermometer), the **safety valve works** (lifted briefly by hand), and the **discharge** is clear.
8. **Document:** the appliance data, the settings, the date and the service plan.

## Tools
Pipe cutter and press or compression tools, level, drill and anchors, thermometer, pressure test pump, a multimeter (for the electrician), tape and PTFE, a container for draining.

## Common mistakes
- **Plugging the safety valve** or no expansion vessel (a dripping valve is a symptom, not a fault to block).
- **Storage temperature too low** (Legionella) or **no scald protection**.
- **Instantaneous unit without checking the panel.**
- **Long dead legs** and no circulation: cold water wait and bacteria.
- **No isolation valves or no drain** for service.
- **A tank on a floor that can't carry it.**

## Quality checks
- Hot water at the farthest tap within the expected time, **temperature at taps ≤ 43 °C** with the mixing valve and **≥ 55 °C in the return**, no leaks, safety valve tested, the **electrician's measurement**.

## Cross-trade
- Plumbing (`plumbing.md`: supply and insulation), heating (`heating.md`: heat source), electrical (`electrical.md`: circuits), sanitary ware (`sanitary.md`: mixers), basement or utility room (`rooms/basement.md`), panel (`panel-and-main-services`).
