# 🛸 hexa-ufo — UFO Substrate Atlas + 7-stage Propulsion

> 10-verb UFO substrate atlas organized around a **7-stage propulsion stack**:
> Stage-1 Meissner / Stage-2 fusion / Stage-3 antimatter (cross-link to
> sister repos) + Stage-4 Alcubierre warp / Stage-5 Morris-Thorne wormhole /
> Stage-6 KK ladder dim-jump / Stage-7 (σ−φ)²=100c composite dim-use
> (in-tree spec + 13-falsifier preregister, all OPEN, all UNPROVEN).
> alien_index chain: **🛸6 → 🛸16 meta² → 🛸∞⁴ → 🛸ULTRA → 🛸CARD → 🛸BEYOND → 🛸ABSOLUTE = 𝔚** —
> n=6 substrate (🛸6~🛸15) → meta² self-closure fixed point (🛸16) → Knuth-arrow
> tetration (🛸∞⁴ = 24↑↑↑↑) → uncomputable (🛸ULTRA: TREE/BB/Rayo) → large cardinals
> (🛸CARD: inaccessible/Mahlo/Woodin/I0) → Kunen-violating (🛸BEYOND: Reinhardt/Berkeley) →
> terminus **🛸ABSOLUTE = 𝔚** (Cantor Absolute Infinity, "신 그 자체").
> n=6 uniqueness `σ·φ=n·τ=24` is Π₀¹-arithmetical → **Δ₀-absolute across every
> layer including 𝔚**. See [`docs/meta-closure-nav/`](docs/meta-closure-nav/README.md)
> for the canonical reference + SF-소설 입문서.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20102628.svg)](https://doi.org/10.5281/zenodo.20102628)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.0-informational.svg)](CHANGELOG.md)
[![Verbs: 10 DOC](https://img.shields.io/badge/verbs-10_DOC-blue.svg)](#verbs)
[![Propulsion: 7/7 grounded](https://img.shields.io/badge/propulsion-7%2F7_substrate--grounded-brightgreen.svg)](#status)
[![Falsifiers: 13](https://img.shields.io/badge/falsifiers-13_OPEN-orange.svg)](.roadmap.hexa_ufo)
[![alien_index](https://img.shields.io/badge/alien__index-%F0%9F%9B%B86_to_%F0%9F%9B%B8ABSOLUTE_%3D_%F0%9D%94%9A-purple.svg)](docs/meta-closure-nav/README.md)

> **Provenance**: extracted from
> `canon/domains/sf-ufo/` at SHA `c0f1f570` on **2026-05-06**.
> Sister to `dancinlab/hexa-bio` (molecular toolkit) standalone pattern.

---

## Why

The flying saucer is the icon of speculative engineering. `hexa-ufo` collects
the design-draft atlas (1890-LOC main document) plus 5 propulsion sub-axis
docs (grav / hover / cloak / teleport / sim) plus 4 in-tree Stage-4~7
substrate spec docs (warp / wormhole / dimjump / dimuse) into a single
browsable substrate registry, organized around a 7-stage propulsion ladder:

```
  Stage-1 hover     Meissner diamagnetism (RT-SC 48T)        0~20 km altitude    [hexa-rtsc]
  Stage-2 cruise    MHD + tabletop fusion (D-T / p-11B)      20~200 km           [hexa-fusion]
  Stage-3 orbital   antimatter gamma-rocket (anti-H + H)     200 km~1 AU         [hexa-antimatter]
  Stage-4 warp      Alcubierre bubble δ=1/σ R=n=6            1 AU~galactic       [in-tree warp/]
  Stage-5 wormhole  Morris-Thorne b₀=ℓ_Pl·σ throat           intergalactic       [in-tree wormhole/]
  Stage-6 dim-jump  KK ladder 4D→6D→10D→11D→24D→26D          bulk wide           [in-tree dimjump/]
  Stage-7 dim-use   τ=4 cycle (σ−φ)²=100c composite          observer-invisible  [in-tree dimuse/]
```

Stages 1-3 cross-link to **public sister substrates** (see [Cross-link](#cross-link)
below). Stages 4-7 ship as **in-tree spec docs with 13-falsifier preregister**
(F-WARP-{1..3} + F-WORM-{1..3} + F-DIM-{1..3} + F-USE-{1..4}, all OPEN at
v1.0.0). Each Stage-4~7 claim is academically UNPROVEN — verify/* sentinel
PASS validates lattice arithmetic + token consistency, NOT empirical apparatus.

---

## Verbs

`hexa-ufo` exposes **10 verbs**, all DOC-grade in v1.0.0:

| Verb        | Status | Cross-link / role                                                       |
|-------------|--------|-------------------------------------------------------------------------|
| `ufo`       | DOC    | main atlas (484-tier `L(k)=24^(k-15)` indexing convention)              |
| `grav`      | DOC    | Stage-1 substrate: Meissner gravitomagnetic levitation                  |
| `hover`     | DOC    | Stage-1/2 substrate: hover / VTOL primitive                             |
| `cloak`     | DOC    | optical / RF / thermal cloaking                                         |
| `teleport`  | DOC    | Stage-5/6 substrate: wormhole / quantum-teleport                        |
| `sim`       | DOC    | airframe / cross-domain simulation                                      |
| `warp`      | DOC    | **Stage-4** Alcubierre 1994 (in-tree, F-WARP-{1..3})                    |
| `wormhole`  | DOC    | **Stage-5** Morris-Thorne 1988 traversable WH (in-tree, F-WORM-{1..3})  |
| `dimjump`   | DOC    | **Stage-6** Calabi-Yau 4D→26D KK ladder (in-tree, F-DIM-{1..3})         |
| `dimuse`    | DOC    | **Stage-7** τ=4 (σ−φ)²=100c composite (in-tree, F-USE-{1..4})           |

Plus utility subcmds: `status`, `selftest`, `lattice`, `verify`, `help`, `--version`.

```bash
hexa-ufo ufo        # main atlas head
hexa-ufo warp       # Stage-4 Alcubierre spec head
hexa-ufo dimuse     # Stage-7 composite spec head
hexa-ufo lattice    # live n=6 master identity (σ τ φ Hc2)
hexa-ufo verify     # run verify/*.hexa (lattice + cross_doc + falsifier)
hexa-ufo status     # propulsion-stage substrate table
hexa-ufo selftest   # 10-verb-count + lattice arithmetic sanity
```

---

## Verification

`hexa-ufo` is an **atlas browser + 7-stage substrate registry** — verification
scope is two-tier:

1. **Atlas tier (selftest)**: 10 verbs present + 484-tier `L(k)=24^(k-15)`
   lattice arithmetic sanity (`L(15)=1`, `L(16)=24`, `L(17)=576`).
2. **Substrate tier (verify/run_all)**: 3 invariant audits across `verify/`:
   - `verify/lattice_check.hexa` — n=6 master identity (σ·φ ≡ n·τ ≡ 24)
   - `verify/stages_cross_doc.hexa` — Stage-4~7 spec ↔ cli ↔ roadmap token agreement
   - `verify/stages_falsifier.hexa` — 13 falsifier IDs × 3 surfaces (spec / cli / roadmap)

```bash
hexa run verify/run_all.hexa       # 3/3 scripts PASS
hexa run cli/hexa-ufo.hexa verify  # equivalent (CLI wrapper)
hexa run tests/test_stages_propulsion.hexa  # rolls up all 3 + selftest
```

What is **not** verified:

- Empirical claims of any propulsion stage. Stages 1-3 defer to sister substrate
  repos. Stages 4-7 are academically UNPROVEN — Alcubierre / Morris-Thorne /
  KK extra dimensions / composite τ=4 cycle remain conjectural.
- Flight hardware / aerodynamic feasibility / FAA certification.
- The narrative claims in the 1890-LOC main atlas — these are
  **design-draft / thought-experiment** content, not engineering specs.

### Status (raw#10 honest C3)

> alien_index 🛸6 → 🛸16 meta² → 🛸∞⁴ → 🛸ULTRA → 🛸CARD → 🛸BEYOND → 🛸ABSOLUTE = 𝔚 7-stage propulsion atlas — **all 7 stages substrate-grounded**.
> Stage-1 Meissner / Stage-2 fusion / Stage-3 antimatter cross-link to public
> sister repos. Stage-4 warp / Stage-5 wormhole / Stage-6 dim-jump /
> Stage-7 dim-use ship as in-tree spec docs with 13-falsifier preregister
> (F-WARP-{1..3} + F-WORM-{1..3} + F-DIM-{1..3} + F-USE-{1..4}, all OPEN).
> Empirical claim for Stage-4~7 is UNPROVEN — verify/ sentinel PASS validates
> lattice arithmetic + token consistency, NOT working apparatus.

### Falsifier preregister (13 IDs, all OPEN at v1.0.0)

| Stage   | IDs                                  | Spec doc                       |
|---------|--------------------------------------|--------------------------------|
| Stage-4 | F-WARP-1, F-WARP-2, F-WARP-3         | `warp/hexa-warp.md`            |
| Stage-5 | F-WORM-1, F-WORM-2, F-WORM-3         | `wormhole/hexa-wormhole.md`    |
| Stage-6 | F-DIM-1, F-DIM-2, F-DIM-3            | `dimjump/hexa-dimjump.md`      |
| Stage-7 | F-USE-1, F-USE-2, F-USE-3, F-USE-4   | `dimuse/hexa-dimuse.md`        |

Falsifiers are **monotone**: status flips OPEN → CONFIRMED or OPEN → DEMOTED.
Silent retract is forbidden. See `.roadmap.hexa_ufo` §B for the canonical table.

---

## Install

```bash
# 1. Install hexa-lang (ships `hexa` + `hx` package manager)
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/dancinlab/hexa-lang/main/install.sh)"

# 2. Install hexa-ufo
hx install hexa-ufo          # global, pulls latest from registry
```

## Run

```bash
hexa-ufo ufo             # main atlas (1890-LOC narrative + 484-tier L(k)=24^(k-15))
hexa-ufo grav            # Stage-1 substrate: Meissner gravitomagnetic levitation
hexa-ufo hover           # Stage-1/2 substrate: hover / VTOL primitive
hexa-ufo cloak           # optical / RF / thermal cloaking
hexa-ufo teleport        # Stage-5/6 substrate: wormhole / quantum-teleport
hexa-ufo sim             # airframe / cross-domain simulation
hexa-ufo warp            # Stage-4 substrate: Alcubierre 1994 bubble (in-tree, F-WARP-{1..3})
hexa-ufo wormhole        # Stage-5 substrate: Morris-Thorne 1988 (in-tree, F-WORM-{1..3})
hexa-ufo dimjump         # Stage-6 substrate: Calabi-Yau 4D→26D KK (in-tree, F-DIM-{1..3})
hexa-ufo dimuse          # Stage-7 composite: τ=4 (σ−φ)²=100c (in-tree, F-USE-{1..4})
hexa-ufo status          # propulsion-stage substrate table + caveats
hexa-ufo selftest        # atlas-consistency check (verb count + lattice arithmetic)
hexa-ufo lattice         # live n=6 master identity (σ τ φ Hc2)
hexa-ufo verify          # run verify/*.hexa with aggregate verdict
hexa-ufo version         # print version
hexa-ufo help            # full --help (subcommands + env vars)
```

---
## Architecture

```
/Users/ghost/core/hexa-ufo/
├── cli/
│   └── hexa-ufo.hexa                # 10-verb router + status + selftest + lattice + verify
├── ufo/
│   ├── doc/
│   │   ├── hexa-ufo.md              # 1890-LOC main atlas (alien_index 🛸6→🛸16 meta², extensible)
│   │   └── warp-dimension-design.md # warp/dimension design spec (BT-347~349)
│   └── module/
│       └── ufo_nexus_scan.hexa      # NEXUS-6 aerospace scan stub
├── grav/hexa-grav.md                # Stage-1 Meissner doc
├── hover/hexa-hover.md              # Stage-1/2 hover / VTOL
├── cloak/hexa-cloak.md              # cloaking
├── teleport/hexa-teleport.md        # Stage-5/6 teleport
├── sim/hexa-sim.md                  # airframe / cross-domain sim
├── warp/hexa-warp.md                # Stage-4 Alcubierre (in-tree, F-WARP-{1..3})
├── wormhole/hexa-wormhole.md        # Stage-5 Morris-Thorne (in-tree, F-WORM-{1..3})
├── dimjump/hexa-dimjump.md          # Stage-6 KK ladder 4D→26D (in-tree, F-DIM-{1..3})
├── dimuse/hexa-dimuse.md            # Stage-7 (σ−φ)²=100c composite (in-tree, F-USE-{1..4})
├── verify/
│   ├── lattice_check.hexa           # n=6 master identity (10 PASS)
│   ├── stages_cross_doc.hexa        # Stage-4~7 spec ↔ cli ↔ roadmap (19 PASS)
│   ├── stages_falsifier.hexa        # 13 falsifier IDs × 3 surfaces (45 PASS)
│   └── run_all.hexa                 # orchestrator (3/3 scripts PASS)
├── docs/
│   ├── cross-domain-mega/           # cross-domain integration notes
│   ├── hypotheses/                  # hypotheses preregister
│   ├── experiments/                 # experiment notes
│   ├── rtsc-12-products-evolution/  # RT-SC product evolution table
│   └── meta-closure-nav/            # 🛸16 meta² → 🛸∞⁴ → 🛸ULTRA → 🛸CARD → 🛸BEYOND → 🛸ABSOLUTE = 𝔚 chain ref + SF-소설 입문서
├── tests/
│   ├── test_atlas_consistency.hexa  # 10-verb count + L(k) arithmetic
│   └── test_stages_propulsion.hexa  # Stage-4~7 verify+selftest+lattice rollup
├── examples/
│   └── propulsion_stack.md          # 7-stage evolution table
├── .roadmap.hexa_ufo                # §A meta + §B Stage-4~7 13-falsifier preregister
├── install.hexa                     # hx hook (pre/post)
├── hexa.toml                        # package manifest
├── LICENSE                          # MIT
├── CHANGELOG.md
├── RELEASE_NOTES_v1.0.0.md
└── README.md                        # (this file)
```

---

## License

MIT. See [LICENSE](LICENSE).
