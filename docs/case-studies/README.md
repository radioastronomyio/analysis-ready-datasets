<!--
---
title: "ARD Case Studies"
description: "Domain-specific ARD implementations"
author: "CrainBramp"
date: "2025-01-06"
version: "1.0"
status: "Active"
tags:
  - type: directory-readme
  - domain: case-study
---
-->

# ARD Case Studies

Domain-specific ARD implementations demonstrating the methodology in practice.

---

## Contents

```
case-studies/
├── desi/           # DESI spectroscopic survey ARD (active)
├── steam/          # Steam Dataset 2025 proto-ARD (retrospective)
└── README.md       # This file
```

---

## Case Studies

| Directory | Domain | Status | Description |
|-----------|--------|--------|-------------|
| [desi/](desi/) | Astronomy | 🔄 Active | ~6.4M extragalactic objects, full layer stack |
| [steam/](steam/) | Gaming | ⬜ Retrospective | Proto-ARD demonstrating cross-domain value |

---

## Adding Case Studies

Each case study directory should contain:

1. **README.md** — Overview, status, key findings
2. **Blueprint documents** — Design specifications (PDFs, specs)
3. **Implementation notes** — Learnings from the build process
4. **Results** — What was achieved, metrics, community engagement

---

## Related

| Document | Relationship |
|----------|--------------|
| [docs/](../README.md) | Parent directory |
| [framework/](../framework/) | Generalized methodology extracted from case studies |
