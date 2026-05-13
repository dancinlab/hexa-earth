# 🌍 hexa-earth — Earth Substrate (HEXA family)

> Earth 묶음 — climate + water + geo + defense 12-verb. A standalone
> packaging of 12 Earth-systems verbs organized into 4 groups, extracted
> from `canon/domains/infra/` at SHA `c0f1f570` (2026-05-06).

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20102604.svg)](https://doi.org/10.5281/zenodo.20102604)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.0-informational.svg)](CHANGELOG.md)
[![Verbs: 12 / 4 groups](https://img.shields.io/badge/verbs-12_/_4_groups-blue.svg)](#verbs)
[![Verify: 4/4 PASS](https://img.shields.io/badge/verify-4%2F4_PASS-brightgreen.svg)](verify/run_all.hexa)
[![Closure: CLOSED](https://img.shields.io/badge/closure-CLOSED-brightgreen.svg)](hexa.toml)
[![Status: SPEC_FIRST](https://img.shields.io/badge/status-SPEC__FIRST-orange.svg)](#status)

---

## Why

`hexa-earth` is the **standalone Earth substrate** in the HEXA family,
collecting 12 verbs across 4 group axes (climate / water / geo / defense)
into a single n=6-aligned bundle. It is the sister of:

- [`dancinlab/hexa-bio`](https://github.com/dancinlab/hexa-bio) — molecular toolkit (4 verbs)
- [`dancinlab/hexa-energy`](https://github.com/dancinlab/hexa-energy) — climate cousin (energy ↔ climate co-design)

The 12-verb / 4-group layout encodes the n=6 invariant lattice's
substrate-level partitioning of Earth-systems concerns:

```
  climate (4)        water (3)         geo (3)            defense (2)
  ───────────        ─────────         ────────           ──────────
  climate            desal             geology            earth_defense
  carbon_capture     desalination      earthquake         hexa_defense
  env_thermal        water_treat       cartography
  env_protect
```

`climate` and `desal/desalination` are intentionally split — they hold
distinct upstream specs (broad-scope vs. operational-impl) that v1.0.0
preserves verbatim for traceability.

---

## Status

**12-verb 통합 substrate (4 그룹: climate + water + geo + defense).
spec-first (작동 .hexa CLI TBD). safety/civil은 후속 standalone
(hexa-safety) 후보.**

- v1.0.0 ships the **canonical extraction of source specs** — verb dirs
  hold the design / spec / docs trees as they existed in
  `canon@c0f1f570`.
- The CLI (`cli/hexa-earth.hexa`) is a **placeholder router** — it lists
  groups, counts verb dirs, runs a 12/12 sentinel selftest. Per-verb
  working `.hexa` implementations are **TBD** (deferred to follow-on cycles).
- `safety` and `civil-engineering` verbs are intentionally **out-of-scope**
  for v1.0.0 and are candidates for a future `hexa-safety` standalone.

This is honest C3 (raw#10): packaging-grade closure, not empirical-grade.

---

## Install

```bash
# 1. Install hexa-lang (gives you `hexa` + `hx` package manager)
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/dancinlab/hexa-lang/main/install.sh)"

# 2. Install hexa-earth
hx install hexa-earth
```

---

## Run

```bash
hexa-earth status              # 12-verb / 4-group presence table + caveats
hexa-earth selftest            # verify 12/12 verb dirs present (sentinel)
hexa-earth --version           # show version
hexa-earth --help              # full usage
```

---

## Verify

Sister-substrate `verify/run_all.hexa` aggregator pattern, scaled to
spec-first 12-verb Earth-substrate scope. From the repo root:

```bash
hexa run verify/run_all.hexa     # exit 0 = all 4 scripts PASS
```

| script                            | what it checks                                                                                  |
| --------------------------------- | ----------------------------------------------------------------------------------------------- |
| `verify/spec_presence.hexa`       | all 12 verb spec docs present at declared paths (4 groups: climate · water · geo · defense)    |
| `verify/lattice_arithmetic.hexa`  | n=6 self-consistency (σ=12 verbs · τ=4 groups · σ·φ = n·τ = 24) — *aux only* per LATTICE_POLICY §1.3 |
| `verify/real_limits_anchor.hexa`  | `LIMIT_BREAKTHROUGH.md` anchors (IPCC AR6 · USGS · NASA-NOAA TSIS-1 · UN-Water · Stefan-Boltzmann · Carnot · Photosynthesis · Shannon) |
| `verify/closure_consistency.hexa` | scoreboard cross-check (CLI · `hexa.toml` · README · `AGENTS.md`) — 12/12 verbs, 4 groups, SPEC_FIRST verdict preserved |

Per [`LATTICE_POLICY.md`](LATTICE_POLICY.md) §1.3, lattice-arithmetic
identities are permitted only as auxiliary self-consistency checks;
the substrate's real verification anchors live in
[`LIMIT_BREAKTHROUGH.md`](LIMIT_BREAKTHROUGH.md) (L1–L7 HARD/SOFT walls
sourced from IPCC AR6 attribution, NASA/NOAA TSIS-1 solar constant,
USGS Mineral Commodity Summaries, UN-Water freshwater availability,
Elimelech & Phillip 2011 desal SEC, and the Stefan / Boltzmann / Carnot
/ Shannon canon). Defense entries remain generic per OPSEC (raw#10 C3 —
no specific weapons-system claims).

---

## Cross-link

- **Sister substrates** (HEXA family standalone repos):
  - [`dancinlab/hexa-bio`](https://github.com/dancinlab/hexa-bio) — Molecular Toolkit (4 verbs)
  - [`dancinlab/hexa-energy`](https://github.com/dancinlab/hexa-energy) — climate cousin (energy ↔ climate co-design)
- **Upstream**: [`canon`](https://github.com/dancinlab/canon) (private) at SHA `c0f1f570`
- **Future siblings** (candidates): `hexa-safety` (safety + civil-engineering),
  `hexa-econ` (economics + currency + governance)

---

## License

MIT — see [LICENSE](LICENSE).

Copyright (c) 2026 박민우 <nerve011235@gmail.com>
