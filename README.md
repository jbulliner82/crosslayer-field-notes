# CrossLayer Field Notes

Public working notes from signal-processing, automation, and systems experiments.

This repository is intentionally append-only in spirit even when a current
note has been revised. Historical state remains part of the record.

## Archive routing convention

A relay key routes into this archive as follows:

1. Normalize the relay key to uppercase exactly as received.
2. SHA-256 the UTF-8 key.
3. The **first hexadecimal digit** selects the archive slot.
4. The **second hexadecimal digit modulo 4** selects revision 0, 1, 2, or 3.
5. Revisions are counted oldest-to-newest within that note's Git history.
6. Recover the ten-character uppercase `FRAGMENT` from the selected revision.

The current version of a note may not be the version a relay key addresses.

## Slot index

| Hex | Field note |
| --- | --- |
| 0 | `archive/00-aperture.md` |
| 1 | `archive/01-carrier.md` |
| 2 | `archive/02-drift.md` |
| 3 | `archive/03-echo.md` |
| 4 | `archive/04-field.md` |
| 5 | `archive/05-glass.md` |
| 6 | `archive/06-horizon.md` |
| 7 | `archive/07-index.md` |
| 8 | `archive/08-junction.md` |
| 9 | `archive/09-kinetic.md` |
| A | `archive/0a-lattice.md` |
| B | `archive/0b-mirror.md` |
| C | `archive/0c-phase.md` |
| D | `archive/0d-relay.md` |
| E | `archive/0e-signal.md` |
| F | `archive/0f-vector.md` |

The archive contains observations, not solutions.
