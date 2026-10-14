# OPENTRONS

![license](https://img.shields.io/badge/license-license-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-scientific_lab-lightgrey)

> Anticloud-hardened packaging of the upstream project `OPENTRONS` in category **SCIENTIFIC LAB**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** SCIENTIFIC LAB · **Upstream:** https://github.com/Opentrons/opentrons · **Upstream pin:** `adb4970a4d170f74b217e947d0176a4f534f298a` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

# Opentrons Platform

## Overview

Opentrons makes robots for biologists.

Our mission is to provide the scientific community with a common platform to easily share protocols and reproduce each other's work. Our robots automate experiments that would otherwise be done by hand, allowing our users to spend more time pursuing answers to the 21st century’s most important questions, and less time pipetting.

This project contains the source code for the Opentrons API and OT App. We'd love for you to to explore, hack, and build upon them!

## Opentrons API

The Opentrons API is a simple framework designed to make writing automated biology lab protocols easy.

We've designed it in a way we hope is accessible to anyone with basic computer and wetlab skills. As a bench scientist, you should be able to code your automated protocols in a way that reads like a lab notebook.

```python
pipette.aspirate(location=trough['A1'], volume=30)
pipette.dispense(location=well_plate['A1'], volume=30)
```

This example tells the Opentrons OT-2 to pipette 30 µL of liquid from a trough to well plate. Learn more here:

- [Documentation](http://docs.opentrons.com)
- [Source code](./api)

## Opentrons App

Easily upload a protocol, calibrate positions, and run your experiment from your computer.

- [Download Here](https://opentrons.com/ot-app)
- [Documentation](https://support.opentrons.com/)
- [Source code](./app)

![The Opentrons App, showing a sortable list of four protocols on the Protocols page. Each entry shows a small map of the OT-2 deck and lists the protocol's name, pipettes and modules used, and when the protocol was updated.](.github/images/opentrons_app.png)

## Opentrons Protocol Designer

Easily create a protocol to run on your robot with this graphical tool.

- [Access Here](https://designer.opentrons.com/)
- [Documentation](https://support.opentrons.com/s/protocol-designer)
- [Source code](./protocol-designer)

## Contributing

We love contributors! Here is the best way to work with us:

1.  Filing a [bug report](https://github.com/Opentrons/opentrons/issues). We will fix these as quickly as we can, and appreciate your help uncovering bugs in our code.

2.  Submit a pull request with any new features you've added to a branch of the API or App. We will reach out to talk with you about integration testing and launching it into our product!

For more information and development setup instructions, please read [the contributing guide][contributing].

Enjoy!

[contributing]: ./CONTRIBUTING.md

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **C/C++ / Make** (manifests: Makefile; scanned in UPSTREAM_CLONE)
- Top-level source layout: `__mocks__/`, `abr-testing/`, `analyses-snapshot-testing/`, `api/`, `api-client/`
- Snapshot size: **1610 files**, **288620 lines of code** (measured; see Benchmarks)
- Primary languages: `.py` (742), `.json` (402), `.ts` (209), `.png` (99), `(none)` (30), `.html` (22)
- Upstream commit pinned for this packaging: `adb4970a4d170f74b217e947d0176a4f534f298a`

---

## Installation

No installation section was found in the upstream readme, so the commands below are generated from the manifests detected in this project directory.

```sh
cmake -B build && cmake --build build    # or: ./configure && make
```

Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

- [Documentation](http://docs.opentrons.com)
- [Source code](./api)

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

The upstream API surface is defined by the `OPENTRONS` source tree vendored in `UPSTREAM_CLONE/` (C/C++ / Make ecosystem). Public entry points:

- Source modules: `__mocks__/`, `abr-testing/`, `analyses-snapshot-testing/`, `api/`, `api-client/`
- The snapshot declares 72 dependency references across 2 ecosystem(s); see Dependencies below.
- Overlay API: `anticloud/cli.py` exposes 13 subcommands with JSON stdout; `anticloud/bench/runner.py` runs the 16-check suite; `anticloud/provenance/chain.py` exposes the SHA3-256 + Ed25519 provenance chain.

---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | C/C++ / Make |
| Manifests detected | Makefile |
| Files in snapshot | 1610 |
| Lines of code | 288620 |
| Dependency references | 72 |
| Dependencies by ecosystem | npm: 4, pypi: 68 |
| Upstream license | Apache-2.0 |
| Overlay license | Anticommons 0.1.0 |

Top dependency references recorded in the benchmark snapshot:

| Ecosystem | Name | Version | Source file |
|-----------|------|---------|-------------|
| npm | @opentrons/shared-data | workspace:* | api-client/package.json |
| npm | @types/lodash | 4.17.24 | api-client/package.json |
| npm | axios | ^0.21.1 | api-client/package.json |
| npm | lodash | 4.18.1 | api-client/package.json |
| pypi | opentrons-shared-data | ==0.0.0 | api/pyproject.toml |
| pypi | numpy | >=1.26.4 | api/pyproject.toml |
| pypi | aionotify | ==0.3.1 | api/pyproject.toml |
| pypi | anyio | >=4.9.0 | api/pyproject.toml |
| pypi | jsonschema | >=3.0.1 | api/pyproject.toml |
| pypi | numpy | >=1.20.0 | api/pyproject.toml |
| pypi | pydantic | >=2.0.0 | api/pyproject.toml |
| pypi | pydantic-settings | >=2 | api/pyproject.toml |
| pypi | pyserial | >=3.5 | api/pyproject.toml |
| pypi | typing-extensions | >=4.0.0 | api/pyproject.toml |
| pypi | click | >=8.0.0 | api/pyproject.toml |
| ... | (57 more) | | |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

No configuration section was found in the upstream readme. Configuration-relevant files detected in this project directory:

- `Dockerfile`
- `Makefile`

Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

*Excerpt from upstream `CONTRIBUTING.md`:*

# Contributing guide

Thanks for your interest in contributing to the Opentrons platform! This Contributing Guide is intended to ensure best practices for both internal Opentrons contributors as well as any external contributors. We want to make sure you’re set up to contribute effectively, no matter if you’re helping us out with bug reports, code, documentation, feature suggestions, or anything else. This guide covers:

- [Opening Issues](#opening-issues)
- [Opening Pull Requests](#opening-pull-requests)
- [PR Etiquette](#pr-etiquette)
- [Commit Guidelines](#commit-guidelines)
- [Project and project Structure](#project-and-project-structure)
- [Development Setup](#development-setup)
- [Robot Environment](#robot-environment)

Other important reading not included in this document:

- [Release processes][]
- [Recommended system setup guide][]

This Contributing Guide was influenced by a lot of work done on existing Contributing Guides. They're great reads if you have the time!

- [React.js Contributing Guide][react-contributing]
- [Node.js Contributing Guide][node-contributing]
- [Kibana Contributing Guide][kibana-contributing]

[release processes]: ./RELEASING.md
[recommended system setup guide]: ./DEV_SETUP.md
[react-contributing]: https://reactjs.org/docs/how-to-contribute.html
[node-contributing]: https://github.com/nodejs/node/blob/master/CONTRIBUTING.md
[kibana-contributing]: https://github.com/elastic/kibana/blob/master/CONTRIBUTING.md

## Opening issues

Please note that the issues tab on this project is disabled. This doesn't mean we don't want to hear from you; it just means that our [support page][support] is a much better way to do so.

## Opening pull requests

If you’d like to contribute code to the Opentrons platform, pull requests (PRs) are the way to do it. Any code contributions are greatly appreciated! If you’re an external contributor, we’re going to assume you are familiar with the fork and pull request flow. If not, this [blog post by Scott Lowe][fork-and-pull] is a good introduction.

Please note that by contributing to the Opentrons platform, you agree to share those contributions under the terms of the [Apache 2.0 license](./LICENSE).

Before opening any PR, please run through the following questions:

- Does this PR address an already open issue?
  - If not, please consider opening an issue first
  - This is to ensure you don't end up duplicating work or wasting time on a PR that won't be accepted
- Does this PR incorporate many 

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: Apache-2.0** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text

                                 Apache License
                           Version 2.0, January 2004
                        http://www.apache.org/licenses/

   TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION

   1. Definitions.

      "License" shall mean the terms and conditions for use, reproduction,
      and distribution as defined by Sections 1 through 9 of this document.

      "Licensor" shall mean the copyright owner or entity authorized by
      the copyright owner that is granting the License.

      "Legal Entity" shall mean the union of the acting entity and all
      other entities that control, are controlled by, or are under common
      control with that entity. For the purposes of this definition,
      "control" means (i) the power, direct or indirect, to cause the
      direction or management of such entity, whether by contract or
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original Apache-2.0 terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `Apache-2.0` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `OPENTRONS` (category: SCIENTIFIC LAB)
- **Upstream URL:** https://github.com/Opentrons/opentrons
- **Pinned commit (SHA):** `adb4970a4d170f74b217e947d0176a4f534f298a`
- **Branch:** edge
- **Pin provenance:** GitHub API commits/<branch> (response quoted in report). The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`8a62bb01f8c4cfc026ee9144a0b672a428509e298b574561ab0f45a5ac2b54ec`.

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

