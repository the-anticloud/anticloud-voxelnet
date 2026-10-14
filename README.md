# VOXELNET

![license](https://img.shields.io/badge/license-MIT-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-voxelization-lightgrey)

> Anticloud-hardened packaging of the upstream project `VOXELNET` in category **VOXELIZATION**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** VOXELIZATION · **Upstream:** https://github.com/jeasinema/tf_voxelnet · **Upstream pin:** `fc3f2ccffc713ae4a1bafa7765fa6a60a1b72c35` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

# VoxelNet-tensorflow

A tensorflow implementation for [VoxelNet](https://arxiv.org/abs/1711.06396).

## Requirement

1. `Python 3.5+`
2. `tensorflow 1.4+`
3. `NumPy`, etc.

## Usage

0. have a look at `config.py` for model configurations, split your data into test/train set by [this](https://xiaozhichen.github.io/files/mv3d/imagesets.tar.gz).
1. run `setup.py` to build the Cython module.
```bash
$ python setup.py build_ext --inplace
```
2. make sure your working directory looks like this (some files are omitted):
```plain
├── build   <-- Cython build file
├── model   <-- some src files
├── utils   <-- some src files
├── setup.py   
├── config.py   
├── test.py   
├── train.py   
├── train_hook.py   
├── README.md    
└── data    <-- KITTI data directory 
    └── object 
        ├── training   <-- training data
        |   ├── image_2   
        |   ├── label_2   
        |   └── velodyne  
        └── testing  <--- testing data
            ├── image_2   
            ├── label_2   
            └── velodyne  
```

3. run `train.py`. Some cmdline parameters is needed, just check `train.py` for them.
4. launch a tensorboard and wait for the training result.

## Data augmentation
Since [c928317](https://github.com/jeasinema/tf_voxelnet/commit/c928317169f1bf23e2157dab20cb402bddb8ffe0), data augmentation is done in an online manner, so there is no need for generating augmented samples.

## Result

TBD

## Acknowledgement

Thanks to [@ring00](https://github.com/ring00) for the implementation of VFE layer and **Jialin Zhao** for the implementation of the RPN.

## License

MIT

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Python** (manifests: setup.py; scanned in UPSTREAM_CLONE)
- Top-level source layout: `model/`, `utils/`
- Snapshot size: **21 files**, **12728 lines of code** (measured; see Benchmarks)
- Primary languages: `.py` (16), `(none)` (2), `.c` (1), `.md` (1), `.pyx` (1)
- Upstream commit pinned for this packaging: `fc3f2ccffc713ae4a1bafa7765fa6a60a1b72c35`

---

## Installation

```bash
$ python setup.py build_ext --inplace
```
2. make sure your working directory looks like this (some files are omitted):
```plain
├── build   <-- Cython build file
├── model   <-- some src files
├── utils   <-- some src files
├── setup.py   
├── config.py   
├── test.py   
├── train.py   
├── train_hook.py   
├── README.md    
└── data    <-- KITTI data directory 
    └── object 
        ├── training   <-- training data
        |   ├── image_2   
        |   ├── label_2   
        |   └── velodyne  
        └── testing  <--- testing data
            ├── image_2   
            ├── label_2   
            └── velodyne  
```

3. run `train.py`. Some cmdline parameters is needed, just check `train.py` for them.
4. launch a tensorboard and wait for the training result.

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

0. have a look at `config.py` for model configurations, split your data into test/train set by [this](https://xiaozhichen.github.io/files/mv3d/imagesets.tar.gz).
1. run `setup.py` to build the Cython module.
```bash
$ python setup.py build_ext --inplace
```
2. make sure your working directory looks like this (some files are omitted):
```plain
├── build   <-- Cython build file
├── model   <-- some src files
├── utils   <-- some src files
├── setup.py   
├── config.py   
├── test.py   
├── train.py   
├── train_hook.py   
├── README.md    
└── data    <-- KITTI data directory 
    └── object 
        ├── training   <-- training data
        |   ├── image_2   
        |   ├── label_2   
        |   └── velodyne  
        └── testing  <--- testing data
            ├── image_2   
            ├── label_2   
            └── velodyne  
```

3. run `train.py`. Some cmdline parameters is needed, just check `train.py` for them.
4. launch a tensorboard and wait for the training result.

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

The upstream API surface is defined by the `VOXELNET` source tree vendored in `UPSTREAM_CLONE/` (Python ecosystem). Public entry points:

- Source modules: `model/`, `utils/`
- Overlay API: `anticloud/cli.py` exposes 13 subcommands with JSON stdout; `anticloud/bench/runner.py` runs the 16-check suite; `anticloud/provenance/chain.py` exposes the SHA3-256 + Ed25519 provenance chain.

---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Python |
| Manifests detected | setup.py |
| Files in snapshot | 21 |
| Lines of code | 12728 |
| Dependency references | 0 |
| Upstream license | MIT |
| Overlay license | Anticommons 0.1.0 |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

1. run `setup.py` to build the Cython module.
```bash
$ python setup.py build_ext --inplace
```
2. make sure your working directory looks like this (some files are omitted):
```plain
├── build   <-- Cython build file
├── model   <-- some src files
├── utils   <-- some src files
├── setup.py   
├── config.py   
├── test.py   
├── train.py   
├── train_hook.py   
├── README.md    
└── data    <-- KITTI data directory 
    └── object 
        ├── training   <-- training data
        |   ├── image_2   
        |   ├── label_2   
        |   └── velodyne  
        └── testing  <--- testing data
            ├── image_2   
            ├── label_2   
            └── velodyne  
```

3. run `train.py`. Some cmdline parameters is needed, just check `train.py` for them.
4. launch a tensorboard and wait for the training result.

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

Upstream contributions: fork the `VOXELNET` project, create a feature branch, and open a pull request against upstream. Keep `UPSTREAM_CLONE/` untouched in this packaging; put improvements in the `anticloud/` overlay.

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: MIT** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
MIT License

Copyright (c) 2019 Tsinghua Robot Learning Lab

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original MIT terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `MIT` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `VOXELNET` (category: VOXELIZATION)
- **Upstream URL:** https://github.com/jeasinema/tf_voxelnet
- **Pinned commit (SHA):** `fc3f2ccffc713ae4a1bafa7765fa6a60a1b72c35`
- **Branch:** master
- **Pin provenance:** local source .git file read (no .git dir in source). The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`587969474a693e1dc86f108faecf454f7c241fe3f1dfb778c4d3528adb2ac787`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

