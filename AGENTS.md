# AGENTS.md

Entry point for AI coding agents working on this repository.

## Project Identity

**Domain:** Analysis Ready Datasets
**Repository:** https://github.com/radioastronomyio/analysis-ready-dataset
**Purpose:** Methodology and knowledge base for creating Analysis Ready Datasets, enhanced materialized datasets that absorb the compute debt of research communities. ARDs transform raw catalog data into queryable products where common derived quantities have been pre-computed.

**Ecosystem:** This repo holds the generalizable methodology. Domain-specific implementations live in their own repos:

| Implementation | Domain | Repository |
|---------------|--------|------------|
| DESI ARD | Astronomy | [desi-cosmic-void-galaxies](https://github.com/radioastronomyio/desi-cosmic-void-galaxies) |
| Steam Dataset 2025 | Gaming | [steam-dataset-2025](https://github.com/radioastronomyio/steam-dataset-2025) |

## Current State

**Phase:** Framework documentation extraction from case studies
**Date:** March 2026

### What Exists

- **Framework documentation** in `docs/framework/` planned, concepts exist in case study PDFs
- **DESI case study** in `docs/case-studies/desi/` with blueprint PDFs in `internal-files/`
- **Steam case study** in `docs/case-studies/steam/` retrospective, planned
- **Research artifacts** in `research/` for GDR outputs and discovery documents
- **Documentation standards** in `docs/documentation-standards/` with templates and tagging strategy
- **Data science infrastructure reference** in `docs/data-science-infrastructure.md`

### What Does NOT Exist Yet

- Generalized framework docs extracted from case studies (concept.md, layer-model.md, discovery-methodology.md)
- Steam retrospective writeup
- Publication draft (methodology paper with case studies)

## The Layer Model

ARDs are built in progressive layers:

| Layer | Contents | Query Patterns Enabled |
|-------|----------|------------------------|
| 0: Raw | Source measurements as released | Basic filtering, aggregation |
| 1: Scalars | Literature-validated derived quantities | Physics-based selection, diagnostics |
| 2: Vectors | Embedding representations | Similarity search, anomaly detection |
| 3: Graphs | Relationship structures | Topological queries, network analysis |

Each layer builds on the one below.

## Key Constraints

- This is a methodology/knowledge base repo, not an implementation repo
- Implementation code lives in domain-specific repos (desi-cosmic-void-galaxies, steam-dataset-2025)
- Framework documentation should be domain-agnostic where possible
- Internal research PDFs in `internal-files/` are working documents, not public-facing

## Execution Environment

**Primary execution:** ML01 (`/opt/repos/analysis-ready-dataset/`)
**Agent runtime:** OpenCode (global config at `~/.config/opencode/opencode.json`)
**Session management:** aoe (Agent of Empires)
**Strategic work:** Claude.ai Projects
**Agentic coding:** Claude Code, OpenCode

## Repository Structure

```
analysis-ready-dataset/
├── assets/                   # Figures, diagrams, banners
├── docs/
│   ├── case-studies/
│   │   ├── desi/             # DESI spectroscopic survey ARD
│   │   └── steam/            # Steam Dataset 2025 proto-ARD
│   ├── documentation-standards/  # Templates and tagging strategy
│   └── framework/            # Generalized ARD methodology
├── internal-files/           # Research PDFs, working documents
├── research/                 # GDR outputs, discovery artifacts
├── shared/                   # Shared resources
├── spec/                     # Specifications (gitignored)
├── staging/                  # Staged work (gitignored)
├── work-logs/                # Development history
├── AGENTS.md                 # This file
├── CLAUDE.md                 # Pointer to AGENTS.md
├── LICENSE                   # MIT (documentation)
├── LICENSE-DATA              # Dataset-specific terms
└── README.md
```

## Conventions

- **Documentation:** Use templates from `docs/documentation-standards/`
- **Commits:** Conventional commits (`feat:`, `fix:`, `docs:`)
- **Frontmatter:** YAML frontmatter with tags from `docs/documentation-standards/tagging-strategy.md`
- **Interior READMEs:** Every directory has one

## Related Repositories

| Repository | Relationship |
|-----------|-------------|
| `desi-cosmic-void-galaxies` | Primary case study implementation |
| `steam-dataset-2025` | Cross-domain validation case study |
| `cosmos2025-anomalies` | Anomaly detection consuming ARD outputs |
| `ai-models-wiki` | References ARD methodology for model governance data |
