<!--
---
title: "ARD Framework"
description: "Core ARD methodology documentation"
author: "CrainBramp"
date: "2025-01-06"
version: "1.0"
status: "Active"
tags:
  - type: directory-readme
  - domain: framework
---
-->

# ARD Framework

Core methodology documentation for Analysis Ready Datasets.

---

## Contents

```
framework/
├── [concept.md]              # What is an ARD (planned)
├── [layer-model.md]          # The four-layer architecture (planned)
├── [discovery-methodology.md]# Materialization discovery approaches (planned)
└── README.md                 # This file
```

---

## Purpose

This directory contains the generalizable ARD methodology—patterns and approaches extracted from case study implementations. Content here is domain-agnostic where possible; domain-specific details live in `../case-studies/`.

---

## Planned Documents

| Document | Description | Status |
|----------|-------------|--------|
| concept.md | What is an ARD, one-time cost philosophy, distinction from VACs | ⬜ Planned |
| layer-model.md | The four-layer architecture (Raw → Scalars → Vectors → Graphs) | ⬜ Planned |
| discovery-methodology.md | Literature-driven and schema-driven materialization discovery | ⬜ Planned |

---

## Current State

Framework documentation will be extracted as the DESI implementation progresses. The foundational concepts exist in the [DESI case study PDFs](../case-studies/desi/); this directory will contain the refined, generalized versions.

---

## Related

| Document | Relationship |
|----------|--------------|
| [docs/](../README.md) | Parent directory |
| [case-studies/](../case-studies/) | Source implementations for methodology extraction |
| [research/](../../research/) | Discovery artifacts informing methodology |
