# Implementation-record template

Date: 2026-11-17

## Problem / Motivation

Every meaningful change in this organisation ships with a record at `docs/implementations/YYYY-MM-DD-<slug>.md`, which explains what was done, why, and how it was checked. The rule is that each record follows a template at `docs/implementations/_TEMPLATE.md`, but no repository had one. Records were written from memory of the required sections, so their structure drifted, and a reader could not tell whether a missing section had been skipped or did not apply.

## What Changed

| File | Change |
|---|---|
| `docs/implementations/_TEMPLATE.md` | New. The template: the seven required sections, with a short note under each on what it must contain. |
| `docs/implementations/2026-11-17-implementation-template.md` | New. This record. |

## Implementation Approach

The template lists the seven sections in their required order: Problem / Motivation, What Changed, Implementation Approach, Mathematical / Statistical Details, Design Decisions, Verification, Related Docs. Each section carries an HTML comment that says what belongs in it. Comments do not render on GitHub, so a record copied from the template and filled in shows only its content.

The same file is added, byte for byte, to `ddr4-udimm`, `spdr` and `.github`, each through its own pull request.

## Design Decisions

- **One template, copied into each repository**, not a single shared file linked from all of them. A contributor working in one repository finds it where the rule says it is, and the rule names a path inside the repository.
- **Comments, not example text.** Placeholder prose left in by mistake would render and read as content. A forgotten comment is invisible.
- **"Does not apply" is said, not implied.** A section that does not apply says so in one line. Only the mathematical section may be deleted outright, for a purely structural change such as this one.
- **Existing records are left as they are.** Older records use their own headings, some numbered. Rewriting them would change the historical record for no gain.

## Verification

1. Open `docs/implementations/_TEMPLATE.md` on GitHub and confirm that the seven headings render in order and the comments do not show.
2. Confirm that this record follows the template.
3. Confirm that the file is identical in all three repositories: `git hash-object docs/implementations/_TEMPLATE.md` gives the same hash in each.

## Related Docs

- Organisation profile: [github.com/Pactolus-Microelectronics](https://github.com/Pactolus-Microelectronics)
