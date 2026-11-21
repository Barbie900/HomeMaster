# HomeMaster renovation project

This folder is a home renovation project managed with the **HomeMaster** plugin.

- Project data lives in `my-home/` (profile, rooms, tools, decisions, log).
- Before any renovation advice, load the `homemaster:knowledge` skill and follow its rules and output formats.
- Answer in the language set in `my-home/profile.md`. If the user asks to switch language, switch everything and update that line in the profile.
- When the user reports finished work, offer to add it to `my-home/log.md` with the date and any measurements.
- When the user makes a choice, offer to record it in `my-home/decisions.md`.
