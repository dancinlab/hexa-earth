<!-- @created: 2026-05-12 -->
<!-- @sister: LATTICE_POLICY.md §1.2 -->
---
project: hexa-earth
domain: Earth substrate — climate + water + geology + earth-defense 12-verb bundle
limits_audited: 7
breakthrough_candidates: 3
hard_walls: 3
soft_walls: 2
unclear: 2
---

# LIMIT_BREAKTHROUGH.md — hexa-earth

## §1 Domain identification

`hexa-earth` is the Earth-systems substrate of the HEXA family, packaging
12 verbs across 4 groups (climate / water / geo / defense) into one
spec-first bundle. Sub-domains include climate modelling, desalination,
geology / earthquake / cartography, civil-engineering, env-thermal,
carbon-capture and earth-defense.

The *infrastructure* nature of hexa-earth: an Earth-systems modelling and
simulation surface whose ceilings are set by the planet itself — energy
balance, hydrological flux, mineral stoichiometry, biosphere capacity.
Real limits are therefore overwhelmingly physical / geochemical /
thermodynamic, with mathematical limits binding the inference that any
climate or geo model can do on finite data.

## §2 Real limits applicable to this project

| # | Limit | Class | Source / value | Applicability to hexa-earth |
|---|-------|-------|----------------|----------------------------|
| L1 | Planetary energy balance | physics | Solar constant S₀ ≈ 1361 W/m² (NASA/NOAA TSIS-1); planetary albedo α ≈ 0.30; net flux (1−α)S₀/4 ≈ 240 W/m² | Hard ceiling on what any Earth climate/energy budget can balance; sets the absolute scale for every climate verb. |
| L2 | Stefan-Boltzmann re-radiation | physics | P = σεAT⁴, σ = 5.67×10⁻⁸ W·m⁻²·K⁻⁴ | Re-radiation to space must close the budget at L1; constrains any geo-engineering / cloud-modification claim to match σεT⁴. |
| L3 | Carnot ceiling (atmospheric heat engine) | physics | η ≤ 1 − T_c/T_h; (T_surface ≈ 288 K, T_tropopause ≈ 220 K) → η_max ≈ 0.24 | Caps the maximum mechanical work the atmosphere/ocean engine can deliver; sets a wind/circulation theoretical ceiling. |
| L4 | Photosynthesis quantum efficiency | physics/bio | Theoretical ≤ ~11 % PAR→biomass; observed C3 ≈ 4.6 %, C4 ≈ 6 % (DOE/USDA) | Caps biosphere primary productivity — binds carbon-capture-by-plants and any nature-based-solution claim. |
| L5 | Mineral reserves & extraction grade | engineering | USGS Mineral Commodity Summaries (Li reserves ≈26 Mt, Cu ≈1.0 Gt, REE ≈110 Mt) | Caps materials available to civil-engineering / earth-defense / desal verbs over project lifetime. |
| L6 | Freshwater availability | engineering | UN World Water Dev. Report — accessible blue water ≈12,500 km³/yr; desal SEC floor ~3 kWh/m³ vs thermodynamic min 0.78 kWh/m³ | Caps the desal verb; the 3.8× ratio above thermodynamic minimum is the soft headroom available before hard wall. |
| L7 | Shannon / statistical-power on climate inference | math | β = f(α, n, effect size); IPCC AR6 attribution requires multi-decadal n | Caps how confidently any climate/earthquake verb can attribute or forecast events from finite observational records. |

(Skipped: lattice anchors — `σ(6)=12`, `τ(6)=4` are organising vocabulary
for the 12-verb / 4-group partitioning, not real limits.)

## §3 Per-limit breakthrough assessment

| Limit | Class | Current state | Breakthrough vector | Trigger metric |
|-------|-------|---------------|---------------------|----------------|
| L1 Solar constant / planetary energy | HARD_WALL | 1361 W/m² is a stellar parameter | None — solar input is a stellar fact, not engineerable | n/a |
| L2 Stefan-Boltzmann re-radiation | HARD_WALL | σεT⁴ is a physical law | None at the physics layer; only ε (effective emissivity) and T can move via geo-engineering | A claim that violates Earth radiative balance ⇒ falsified |
| L3 Carnot on atmospheric engine | HARD_WALL | ~24 % ceiling, current circulation realises ~2 % | None for η_max; engineering can approach the ceiling but not pass | A simulator claiming ocean/atmosphere η > 24 % ⇒ falsified |
| L4 Photosynthesis efficiency | SOFT_WALL | C3 ≈ 4.6 % vs theoretical ≤ 11 % | Synthetic-bio (C4 retrofit, RuBisCO redesign, cyanobacterial chassis), photo-electro-chemical artificial leaves | Demonstrated PAR→stored-C ≥ 8 % in open-field trial |
| L5 Mineral reserves | SOFT_WALL | USGS reserves are static-economic; resources >> reserves | Higher grade extraction, deep-sea / lunar / asteroid mining (couples to `hexa-space`), recycling rate >> primary | Verified reserve-to-production ratio rising under demand |
| L6 Freshwater / desal SEC | BREAKABLE_WITH_TECH | 3 kWh/m³ SOTA; thermodynamic min 0.78 kWh/m³ | Forward-osmosis hybrids, advanced membranes, brine-mined-mineral co-production, waste-heat coupling | SEC ≤ 1.5 kWh/m³ at MED scale |
| L7 Climate statistical power | UNCLEAR | Power rises with n; signal-to-noise improves under continued warming | Longer obs records, paleoclimate proxies, ensemble ML emulators, satellite constellation density | Detection power β ≥ 0.8 at α = 0.05 for sub-regional events |

## §4 Top-3 breakthrough opportunities (this project)

1. **L6 — Desal SEC.** The 3.8× gap between SOTA (~3 kWh/m³) and the
   thermodynamic floor (~0.78 kWh/m³, IDA + Elimelech 2011) is the most
   tractable engineering lever in the bundle. Hexa-earth's `desal/` verb
   should anchor on the floor and report achieved vs theoretical, not
   on lattice partition. Concrete trigger: report SEC ≤ 1.5 kWh/m³ in
   MED-scale trial. Risk: medium (membrane stability).
2. **L4 — Photosynthesis efficiency lift via synthetic bio.** A 4.6 % →
   8 % field lift roughly doubles the carbon-capture verb's natural-
   solution ceiling. Honest framing: this is not "breakthrough physics"
   but climbing within an existing physical ceiling. Risk: high
   (regulatory + ecological).
3. **L7 — Statistical-power improvement on attribution.** A model-
   evaluation rig that reports β (power) alongside p, on each
   `climate/`/`earthquake/` claim, raises the verification rigour
   without any new physics. Risk: zero (analysis-only); reputation
   upside high.

## §5 Honest caveats (raw#10 C3)

- L1–L3 are HARD physical laws; any verb output that violates radiative
  or thermodynamic balance is falsified, regardless of how elegant the
  lattice-fit looks.
- The "12 verbs / 4 groups" partition is organisational vocabulary, NOT
  a real Earth-systems limit. Real ceilings (S₀, σT⁴, USGS reserves)
  set the binding constraints.
- "Mineral reserves" (L5) are *economic*; under different prices /
  technologies the boundary moves. The HARD wall is total crustal
  abundance (Clarke values), which sits 10²–10⁴× above current reserves
  for most metals. Hexa-earth should not conflate the two.
- IPCC AR6 attribution power (L7) is rising over time because the
  forced signal is rising — the "breakthrough" here is partially
  *getting the climate change we are trying to avoid*. Stated bluntly
  for honesty.
- No claim is made that hexa-earth's 12-verb structure follows any
  external Earth-system invariant. The lattice anchors are internal
  organising vocabulary only (LATTICE_POLICY §1.3).

## §6 References

- `LATTICE_POLICY.md` §1.2 (universal real-limits standard, 2026-05-12)
- NASA / NOAA TSIS-1 — Total Solar Irradiance Sensor (1361 W/m²)
- IPCC AR6 WG1 — radiative forcing, attribution methodology
- USGS Mineral Commodity Summaries 2024 — reserves & resources
- UN-Water World Water Development Report 2024
- Elimelech & Phillip, "The Future of Seawater Desalination," *Science* 333, 712 (2011)
- Zhu, Long, Ort, *Annu. Rev. Plant Biol.* 61, 235 (2010) — photosynthesis efficiency
- Stefan (1879), Boltzmann (1884), Carnot (1824), Shannon (1948)
