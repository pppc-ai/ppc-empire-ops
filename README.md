# PPC Empire Ops

Live workspace for building and monitoring the PPC empire under a $5/day API spend constraint.

## Structure
- `ops/` – Ledger, status board, security map, machine-readable state for the dashboard.
- `experiments/` – One folder per revenue experiment (plans, prompts, outputs, retros).
- `dashboard/` – Static site deployed to GitHub Pages for real-time observability.
- `.secrets/` – Local-only credentials (ignored by git).

## Observability
- Update `ops/state.json` + `ops/status.md` whenever initiatives move.
- Run ledger entries for each API usage or revenue event.
- GitHub Pages auto-build reflects the latest committed state.
