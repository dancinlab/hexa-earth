# hexa-earth v1.0.0 — Earth Substrate (HEXA family)

**Release date**: 2026-05-06
**Closure verdict**: **SPEC_FIRST** (12 verb dirs extracted; working `.hexa`
CLI per verb is TBD)
**Provenance**: extracted 2026-05-06 from
`canon/domains/infra/` at SHA `c0f1f570`. Sister of
`hexa-bio` (registry L24) and `hexa-energy` (climate cousin).

This is the **initial standalone release** of `hexa-earth`, a 12-verb
Earth substrate organized into 4 group axes (climate + water + geo + defense)
under the n=6 invariant lattice.

## Highlights

- **12-verb / 4-group layout** preserved from upstream:
  - climate (4): `climate`, `carbon_capture`, `env_thermal`, `env_protect`
  - water (3): `desal`, `desalination`, `water_treat`
  - geo (3): `geology`, `earthquake`, `cartography`
  - defense (2): `earth_defense`, `hexa_defense` (peaceful-only)
- **CLI placeholder** — `cli/hexa-earth.hexa` ships a working `status` /
  `selftest` / `help` / `version` router. Per-verb subcommands are deferred.
- **Selftest** — 12-verb directory presence sweep
  (`__HEXA_EARTH_SELFTEST__ PASS` sentinel).
- **MIT license** — permissive distribution.
- **GitHub-only distribution** — canonical at
  <https://github.com/dancinlab/hexa-earth>.

## Quickstart

```bash
git clone https://github.com/dancinlab/hexa-earth.git ~/.hexa-earth
export HEXA_EARTH_ROOT=~/.hexa-earth
hexa run $HEXA_EARTH_ROOT/cli/hexa-earth.hexa selftest
hexa run $HEXA_EARTH_ROOT/cli/hexa-earth.hexa status
```

## Honest caveats (raw#10 C3)

1. **Spec-first**: verb dirs hold canonical specs from
   `canon@c0f1f570`; per-verb working `.hexa` implementations are
   TBD in follow-on cycles.
2. **Peaceful-only defense scope**: `earth_defense` and `hexa_defense` are
   locked to planetary-defense / civil-resilience use cases (no offensive
   systems). Inherits the upstream `critical-mineral-conflict-arbitration`
   peaceful-only reframing.
3. **Deferred verbs**: `safety` and `civil-engineering` upstream domains
   are intentionally out-of-scope for v1.0.0; candidates for a future
   `hexa-safety` standalone.
4. **n=6 lattice claim**: the 4-group / 12-verb partitioning is hypothesized
   under the n=6 invariant; empirical grounding is per-verb future work.

## Cross-link

- Sister: [`hexa-bio`](https://github.com/dancinlab/hexa-bio)
  (Molecular Toolkit, 4 verbs)
- Climate cousin: [`hexa-energy`](https://github.com/dancinlab/hexa-energy)
  (energy ↔ climate co-design)
- Upstream: `canon` (private) @ `c0f1f570`
