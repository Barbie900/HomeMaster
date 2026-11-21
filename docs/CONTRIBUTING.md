# Contributing

## Knowledge rules
1. **Be specific.** Give numbers with units (mm, %, CM-%, hours, bar), product classes (e.g. tile adhesive `C2TE S1`, grout `CG2WA`) and the standard they come from (EN 12004, EN 13888, EN 14891, IEC 60364-7-701, …). Don't recommend brands.
2. **Say when it depends.** If a value varies by product, write the typical range and "follow the data sheet".
3. **Every new task goes into `dependencies.yaml`**, with its `requires`, `blocks` and `wait_after`. A task with no dependencies is almost always missing some.
4. **Safety first.** Anything that can hurt someone or is legally restricted gets `severity: critical` and a note that it is the safety reviewer's job.
5. **Keep regional facts in region files.** Regulations, store chains and local customs go in `references/regions/<cc>.md`, not in trade files.

## Adding a language
- `skills/knowledge/references/glossary-<lang>.md`: trade terms EN ↔ your language
- `skills/knowledge/references/regions/<cc>.md`: regulations, licensing, local practice
- Add display names in `dependencies.yaml` (`name: {en: …, <lang>: …}`)
