<!--
---
title: "DESI ARD Case Study"
description: "Analysis Ready Dataset for the DESI spectroscopic survey"
author: "CrainBramp"
date: "2025-01-06"
version: "1.0"
status: "Active"
tags:
  - type: case-study
  - domain: case-study
  - tech: [desi, bagpipes, disperse, embeddings]
---
-->

# DESI ARD Case Study

Analysis Ready Dataset implementation for the Dark Energy Spectroscopic Instrument.

---

## Contents

```
desi/
├── DESI_ARD__Embeddings__Physics__Topology.pdf   # Blueprint document (pending)
├── Storage_Deep_Dive_and_Schema_Justification.pdf # Schema specification (pending)
└── README.md                                      # This file
```

---

## Overview

The DESI ARD transforms the cosmic voids Value-Added Catalog (~6.4M extragalactic objects) into a full analysis-ready product with pre-computed physics scalars, spectral embeddings, and cosmic web topology.

**Implementation Repository:** [desi-cosmic-void-galaxies](https://github.com/radioastronomyio/desi-cosmic-void-galaxies)

---

## Status

| Layer | Status | Contents |
|-------|--------|----------|
| 0: Raw | ✅ Complete | 6.4M objects in PostgreSQL with environmental classification |
| 1: Scalars | 🔄 In Progress | Literature-validated materializations via GDR discovery |
| 2: Vectors | ⬜ Planned | Universal Spectrum Tokenizer, AstroCLIP embeddings |
| 3: Graphs | ⬜ Planned | Cosmic web topology, k-NN proximity |

---

## Blueprint Documents

| Document | Description |
|----------|-------------|
| DESI_ARD__Embeddings__Physics__Topology.pdf | The "Perfect ARD" blueprint—layers, models, scientific use cases |
| Storage_Deep_Dive_and_Schema_Justification.pdf | Architectural defense, schema specification for edge hardware |

---

## Key Specifications

From the blueprint documents:

| Aspect | Specification |
|--------|---------------|
| Target hardware | 4-node cluster, 144GB RAM, 16GB VRAM (A4000), SATA SSDs |
| Storage format | Apache Parquet (metadata), HDF5 (spectra) |
| Embedding models | Universal Spectrum Tokenizer (~300M params), AstroCLIP (~43M) |
| Topology | DisPerSE with domain decomposition |

---

## Related

| Document | Relationship |
|----------|--------------|
| [case-studies/](../README.md) | Parent directory |
| [research/](../../../research/) | GDR outputs for materialization discovery |
| [framework/](../../framework/) | Generalized methodology |
