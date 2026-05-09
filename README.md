# 🌍 hexa-earth — Earth Substrate (HEXA family)

> Earth 묶음 — climate + water + geo + defense 12-verb. A standalone
> packaging of 12 Earth-systems verbs organized into 4 groups, extracted
> from `canon/domains/infra/` at SHA `c0f1f570` (2026-05-06).

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.0-informational.svg)](CHANGELOG.md)
[![Verbs: 12 / 4 groups](https://img.shields.io/badge/verbs-12_/_4_groups-blue.svg)](#verbs)
[![Status: SPEC_FIRST](https://img.shields.io/badge/status-SPEC__FIRST-orange.svg)](#status)

---

## Why

`hexa-earth` is the **standalone Earth substrate** in the HEXA family,
collecting 12 verbs across 4 group axes (climate / water / geo / defense)
into a single n=6-aligned bundle. It is the sister of:

- [`need-singularity/hexa-bio`](https://github.com/need-singularity/hexa-bio) — molecular toolkit (4 verbs)
- [`need-singularity/hexa-energy`](https://github.com/need-singularity/hexa-energy) — climate cousin (energy ↔ climate co-design)

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

## Verbs

### climate group (4)

| verb              | upstream source                                                       |
|-------------------|-----------------------------------------------------------------------|
| `climate/`        | `canon/domains/infra/climate/`                              |
| `carbon_capture/` | `canon/domains/infra/carbon-capture/`                       |
| `env_thermal/`    | `canon/domains/infra/environment-thermal/`                  |
| `env_protect/`    | `canon/domains/infra/environmental-protection/`             |

### water group (3)

| verb            | upstream source                                                       |
|-----------------|-----------------------------------------------------------------------|
| `desal/`        | `canon/domains/infra/desal/`                                |
| `desalination/` | `canon/domains/infra/desalination/`                         |
| `water_treat/`  | `canon/domains/infra/water-treatment/`                      |

### geo group (3)

| verb           | upstream source                                                       |
|----------------|-----------------------------------------------------------------------|
| `geology/`     | `canon/domains/infra/geology/`                              |
| `earthquake/`  | `canon/domains/infra/earthquake-engineering/`               |
| `cartography/` | `canon/domains/infra/cartography-gis/`                      |

### defense group (2) — peaceful-only

| verb             | upstream source                                                     |
|------------------|---------------------------------------------------------------------|
| `earth_defense/` | `canon/domains/infra/earth-defense/`                      |
| `hexa_defense/`  | `canon/domains/infra/hexa-defense/`                       |

The defense group is **locked to peaceful planetary-defense scope**
(asteroid impact mitigation, climate-shield, civil resilience). No
offensive systems. This inherits from the upstream
`critical-mineral-conflict-arbitration` peaceful-only reframing
(`canon` commit `c0f1f570`).

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
# git clone (works today):
git clone https://github.com/need-singularity/hexa-earth.git ~/.hexa-earth
export HEXA_EARTH_ROOT=~/.hexa-earth
export PATH="$HEXA_EARTH_ROOT/cli:$PATH"

# Run any subcommand:
hexa run $HEXA_EARTH_ROOT/cli/hexa-earth.hexa status
hexa run $HEXA_EARTH_ROOT/cli/hexa-earth.hexa selftest
```

Future: `hx install hexa-earth` once the hexa-lang registry entry lands.

---

## Cross-link

- **Sister substrates** (HEXA family standalone repos):
  - [`need-singularity/hexa-bio`](https://github.com/need-singularity/hexa-bio) — Molecular Toolkit (4 verbs)
  - [`need-singularity/hexa-energy`](https://github.com/need-singularity/hexa-energy) — climate cousin (energy ↔ climate co-design)
- **Upstream**: [`canon`](https://github.com/need-singularity/canon) (private) at SHA `c0f1f570`
- **Future siblings** (candidates): `hexa-safety` (safety + civil-engineering),
  `hexa-econ` (economics + currency + governance)

---

## License

MIT — see [LICENSE](LICENSE).

Copyright (c) 2026 박민우 <nerve011235@gmail.com>
