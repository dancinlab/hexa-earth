# Changelog

All notable changes to **hexa-earth** are documented here. Format follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and SemVer.

## [1.0.0] - 2026-05-06

### Added

- Initial extraction from `canon/domains/infra/` at SHA `c0f1f570`.
- 12-verb / 4-group Earth substrate:
  - climate group (4): `climate`, `carbon_capture`, `env_thermal`, `env_protect`
  - water group (3): `desal`, `desalination`, `water_treat`
  - geo group (3): `geology`, `earthquake`, `cartography`
  - defense group (2): `earth_defense`, `hexa_defense` (peaceful-only)
- `cli/hexa-earth.hexa` placeholder router (status / selftest / help / version).
- `install.hexa` hx-package-manager hook (post-install selftest, warn-only).
- `hexa.toml` v1.0.0 manifest (MIT license; closure verdict `SPEC_FIRST`).
- `tests/test_selftest.hexa` — 12-verb directory count assertion.
- MIT `LICENSE`.
- Cross-link to sister repos (`hexa-bio`, `hexa-energy`).

### Honest scope (raw#10 C3)

- v1.0.0 is **spec-first** — working per-verb `.hexa` CLI implementations
  are TBD.
- Defense group is locked to **peaceful planetary-defense scope** only.
- `safety` / `civil-engineering` verbs are intentionally **deferred** to a
  candidate future `hexa-safety` standalone.
