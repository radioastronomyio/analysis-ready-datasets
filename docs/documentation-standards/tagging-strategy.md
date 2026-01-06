<!--
---
title: "ARD Tagging Vocabulary"
description: "Controlled vocabulary for document classification in the ARD repository"
author: "CrainBramp"
date: "2025-01-06"
version: "1.0"
status: "Active"
tags:
  - type: reference
  - domain: documentation
---
-->

# ARD Tagging Vocabulary

Controlled vocabulary for YAML frontmatter tags in the Analysis Ready Datasets repository. Consistent tagging enables navigation and RAG retrieval.

---

## Type Tags

What kind of document is this?

| Tag | Use For |
|-----|---------|
| `project-root` | Repository root README |
| `directory-readme` | README for a directory (interior READMEs) |
| `methodology` | ARD methodology documentation (layer model, discovery approaches) |
| `specification` | Formal definitions (schema specs, data dictionaries) |
| `guide` | Step-by-step procedures (how to build an ARD) |
| `reference` | Lookup information (tag vocabularies, templates) |
| `research-output` | GDR outputs, literature reviews, discovery artifacts |
| `case-study` | Domain-specific ARD implementation documentation |
| `worklog` | Work session documentation |

---

## Domain Tags

What subject area does this cover?

| Tag | Description |
|-----|-------------|
| `framework` | Core ARD methodology, layer model, general patterns |
| `case-study` | Domain-specific implementations (DESI, Steam) |
| `research` | Discovery artifacts, GDR outputs, literature analysis |
| `documentation` | Meta-documentation (templates, standards, this file) |

---

## Tech Tags

What technologies are involved? Use when the document focuses on specific tools.

### Storage & Data

| Tag | Description |
|-----|-------------|
| `postgresql` | PostgreSQL database, pgvector |
| `parquet` | Apache Parquet columnar storage |
| `hdf5` | HDF5 hierarchical data format |

### ML & Embeddings

| Tag | Description |
|-----|-------------|
| `embeddings` | Vector embeddings generally |
| `bge-m3` | BGE-M3 embedding model |
| `astroclip` | AstroCLIP multimodal model |
| `universal-tokenizer` | Universal Spectrum Tokenizer |

### Physics & Astronomy

| Tag | Description |
|-----|-------------|
| `bagpipes` | Bayesian SED fitting |
| `ppxf` | Penalized pixel-fitting kinematics |
| `disperse` | Cosmic web topology |
| `desi` | Dark Energy Spectroscopic Instrument |

---

## Status Tags

What's the document lifecycle state?

| Tag | Description |
|-----|-------------|
| `draft` | In development, not yet complete |
| `active` | Current, maintained |
| `deprecated` | Superseded, avoid for new work |
| `archived` | Historical reference only |

---

## Audience Tags

Who is this for? Use when not obvious from context.

| Tag | Description |
|-----|-------------|
| `implementers` | People building ARDs |
| `researchers` | People using ARD data products |
| `all` | General audience |

---

## Usage Examples

### Framework Methodology Document

```yaml
tags:
  - type: methodology
  - domain: framework
  - status: active
```

### DESI Case Study Document

```yaml
tags:
  - type: case-study
  - domain: case-study
  - tech: [desi, bagpipes, disperse]
  - status: active
```

### GDR Research Output

```yaml
tags:
  - type: research-output
  - domain: research
  - tech: desi
  - status: active
```

### Directory README

```yaml
tags:
  - type: directory-readme
  - domain: framework
```

---

## Conventions

- Use lowercase, hyphenated values (`research-output` not `ResearchOutput`)
- Tech tags use canonical short names (`postgresql` not `postgres` or `PostgreSQL`)
- One value per line for single tags, array syntax for multiple: `tech: [desi, bagpipes]`
- Omit optional categories if not applicable (don't add empty tags)

---

## Adding New Tags

1. Check if existing tag covers the concept
2. If not, add to appropriate section in this document
3. Include one-sentence description
4. Backfill existing documents if the new tag applies retroactively
