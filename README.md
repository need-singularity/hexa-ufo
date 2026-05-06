# 🛸 hexa-ufo — UFO Substrate Atlas + 7-stage Propulsion

> 6-verb UFO substrate atlas organized around a **7-stage propulsion stack**:
> Stage-1 Meissner / Stage-2 fusion / Stage-3 antimatter (substrate-grounded
> via sister repos) → Stage-4 warp / Stage-5 wormhole / Stage-6 dim-jump /
> Stage-7 dim-use (TBD — no public substrate exists yet).
> alien_index spans **6 → 500** across a 484-tier `L(k)=24^(k-15)` lattice.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.0-informational.svg)](CHANGELOG.md)
[![Verbs: 6 DOC](https://img.shields.io/badge/verbs-6_DOC-blue.svg)](#verbs)
[![Propulsion: 3/7 grounded](https://img.shields.io/badge/propulsion-3%2F7_substrate--grounded-orange.svg)](#status)
[![alien_index](https://img.shields.io/badge/alien__index-6_to_500-purple.svg)](#status)

> **Provenance**: extracted from
> `n6-architecture/domains/sf-ufo/` at SHA `c0f1f570` on **2026-05-06**.
> Sister to `need-singularity/hexa-bio` (molecular toolkit) standalone pattern.

---

## Why

The flying saucer is the icon of speculative engineering. `hexa-ufo` collects
the design-draft atlas (1890-LOC main document) plus 5 propulsion sub-axis
docs (grav / hover / cloak / teleport / sim) into a single browsable
substrate registry, organized around a 7-stage propulsion ladder:

```
  Stage-1 hover     Meissner diamagnetism (RT-SC 48T)        0~20 km altitude
  Stage-2 cruise    MHD + tabletop fusion (D-T / p-11B)      20~200 km
  Stage-3 orbital   antimatter gamma-rocket (anti-H + H)     200 km~1 AU
  Stage-4 warp      Alcubierre bubble                        1 AU~galactic   [TBD]
  Stage-5 wormhole  Morris-Thorne ER bridge                  intergalactic   [TBD]
  Stage-6 dim-jump  KK-tower 4.8 TeV brane transit           bulk wide       [TBD]
  Stage-7 dim-use   Calabi-Yau 6-fold navigation             observer-invisible [TBD]
```

Stages 1-3 cross-link to **public sister substrates** (see [Cross-link](#cross-link)
below). Stages 4-7 ship as TBD — no public substrate exists yet.

---

## Verbs

`hexa-ufo` exposes **6 verbs**, all DOC-grade in v1.0.0:

| Verb       | Status | Doc LOC | Cross-link / role                                          |
|------------|--------|---------|------------------------------------------------------------|
| `ufo`      | DOC    | 1890    | main atlas (484-tier `L(k)=24^(k-15)` indexing convention) |
| `grav`     | DOC    | 653     | Stage-1 substrate: Meissner gravitomagnetic levitation     |
| `hover`    | DOC    | 457     | Stage-1/2 substrate: hover / VTOL primitive                |
| `cloak`    | DOC    | 471     | optical / RF / thermal cloaking                            |
| `teleport` | DOC    | 440     | Stage-5/6 substrate: wormhole / quantum-teleport           |
| `sim`      | DOC    | 614     | airframe / cross-domain simulation                         |

Plus utility subcmds: `status`, `selftest`, `help`, `--version`.

```bash
hexa-ufo ufo        # main atlas head
hexa-ufo grav       # Stage-1 doc head
hexa-ufo status     # propulsion-stage substrate table
hexa-ufo selftest   # verb-count + lattice arithmetic sanity
```

---

## Verification

`hexa-ufo` is an **atlas browser** — verification scope is intentionally narrow:

1. **6 verbs present** (`ufo / grav / hover / cloak / teleport / sim`), each
   with a non-empty markdown doc. Checked by `hexa-ufo selftest`.
2. **484-tier `L(k)=24^(k-15)` lattice arithmetic** sanity:
   `L(15)=1`, `L(16)=24`, `L(17)=576`. Checked by `hexa-ufo selftest`.

What is **not** verified:

- Empirical claims of any propulsion stage (Stages 1-3 defer to sister substrate
  repos for empirical verification; Stages 4-7 are TBD).
- Flight hardware / aerodynamic feasibility / FAA certification.
- The narrative claims in the 1890-LOC main atlas — these are
  **design-draft / thought-experiment** content, not engineering specs.

### Status (raw#10 honest C3)

> alien_index 6→500 7-stage propulsion atlas
> (Stage-1 Meissner / Stage-2 fusion / Stage-3 antimatter /
>  Stage-4 warp / Stage-5 wormhole / Stage-6 dimension /
>  Stage-7 dimensional-use).
> Stages 4~7는 공개 substrate 미존재 — TBD.
> 1890 LOC main atlas + propulsion 6-verb.

---

## Install

### Via `hx` (recommended)

```bash
hx install hexa-ufo          # global, pulls latest from registry
hx install hexa-ufo@1.0.0    # pin specific version
hexa-ufo --version           # → 1.0.0
```

### Via git clone (works today)

```bash
git clone https://github.com/need-singularity/hexa-ufo.git ~/.hexa-ufo
export HEXA_UFO_ROOT=~/.hexa-ufo
export PATH="$HEXA_UFO_ROOT/cli:$PATH"

# Run any subcommand:
hexa run $HEXA_UFO_ROOT/cli/hexa-ufo.hexa selftest
hexa run $HEXA_UFO_ROOT/cli/hexa-ufo.hexa status
hexa run $HEXA_UFO_ROOT/cli/hexa-ufo.hexa ufo
```

No Python deps. No network. Pure-hexa atlas browser.

---

## Cross-link

`hexa-ufo` is the **substrate-atlas hub** — the actual physical substrates
live in 4 sister `need-singularity` repos:

| Stage   | Substrate                | Sister repo (public, GitHub)                                                 |
|---------|--------------------------|------------------------------------------------------------------------------|
| Stage-1 | RT-SC Meissner 48T coil  | <https://github.com/need-singularity/hexa-rtsc>                              |
| Stage-2 | tabletop D-T / p-11B fusion power | <https://github.com/need-singularity/hexa-fusion>                   |
| Stage-3 | antimatter (anti-H) propulsion fuel | <https://github.com/need-singularity/hexa-antimatter>             |
| Stage-3 aux | onboard sigma-cascade accelerator | <https://github.com/need-singularity/petite-cern>                |

Stages 4-7 (warp / wormhole / dim-jump / dim-use) have **no public sister
substrate** — they remain TBD pending future extraction (or pending the
existence of the underlying physics).

---

## Architecture

```
/Users/ghost/core/hexa-ufo/
├── cli/
│   └── hexa-ufo.hexa                # 6-verb router + status + selftest
├── ufo/
│   ├── doc/
│   │   ├── hexa-ufo.md              # 1890-LOC main atlas (alien_index 6→500)
│   │   └── warp-dimension-design.md # warp/dimension design spec
│   └── module/
│       └── ufo_nexus_scan.hexa      # NEXUS-6 aerospace scan stub
├── grav/hexa-grav.md                # Stage-1 Meissner doc (653 LOC)
├── hover/hexa-hover.md              # Stage-1/2 hover / VTOL (457 LOC)
├── cloak/hexa-cloak.md              # cloaking (471 LOC)
├── teleport/hexa-teleport.md        # Stage-5/6 teleport (440 LOC)
├── sim/hexa-sim.md                  # airframe / cross-domain sim (614 LOC)
├── docs/
│   ├── cross-domain-mega/           # cross-domain integration notes
│   ├── hypotheses/                  # hypotheses preregister
│   ├── experiments/                 # experiment notes
│   └── rtsc-12-products-evolution/  # RT-SC product evolution table
├── tests/
│   └── test_atlas_consistency.hexa  # verb count + lattice arithmetic
├── examples/
│   └── propulsion_stack.md          # 7-stage evolution table
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
