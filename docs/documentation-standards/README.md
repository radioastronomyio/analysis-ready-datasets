<!--
---
title: "Documentation Standards"
description: "Templates and guidelines for ARD documentation"
author: "CrainBramp"
date: "2025-01-06"
version: "1.0"
status: "Active"
tags:
  - type: directory-readme
  - domain: documentation
---
-->

# Documentation Standards

Templates and vocabulary for ARD repository documentation.

---

## Contents

```
documentation-standards/
├── primary-readme-template.md    # Repository root README
├── interior-readme-template.md   # Directory README
├── general-kb-template.md        # Standalone documents
├── worklog-readme-template.md    # Work session directories
├── tagging-strategy.md           # Tag vocabulary for this repo
└── README.md                     # This file
```

---

## Templates

| Template | Use For |
|----------|---------|
| [primary-readme-template.md](primary-readme-template.md) | Repository root README.md |
| [interior-readme-template.md](interior-readme-template.md) | Any directory that needs a README |
| [general-kb-template.md](general-kb-template.md) | Standalone documents (methodology, specs, guides) |
| [worklog-readme-template.md](worklog-readme-template.md) | Activity directories in `work-logs/` |

---

## Vocabulary

| Document | Purpose |
|----------|---------|
| [tagging-strategy.md](tagging-strategy.md) | Controlled tag vocabulary for YAML frontmatter |

---

## Template Selection

```
Is it the repository root README?
├─ Yes → primary-readme-template.md
└─ No: Is it a directory README?
        ├─ Yes: Is it a work-logs activity?
        │       ├─ Yes → worklog-readme-template.md
        │       └─ No  → interior-readme-template.md
        └─ No: Is it a standalone document?
                └─ Yes → general-kb-template.md
```

---

## Related

| Document | Relationship |
|----------|--------------|
| [docs/](../README.md) | Parent directory |
