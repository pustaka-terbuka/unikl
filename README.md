# Pustaka Terbuka — UNIKL (Universiti Kuala Lumpur Library)

> **Pustaka Terbuka: Katalog Induk Terbuka untuk Perpustakaan dan Sekolah Malaysia.**  
> *Official Universiti Kuala Lumpur Library (UNIKL) Bibliographic Dataset & Standalone Harvester.*

This repository contains the harvested open MARCXML collection and harvester pipeline for **Universiti Kuala Lumpur Library** (`UNIKL`), contributing to the national Malaysian union catalog at [pustaka-terbuka/opac](https://github.com/pustaka-terbuka/opac).

---

## Institutional Metadata

| Attribute | Value |
| :--- | :--- |
| **Institution Code** | `unikl` |
| **Agency Code** | `UNIKL` |
| **Official Name** | Universiti Kuala Lumpur Library |
| **Institution Type** | `university` |
| **State / Territory** | Kuala Lumpur |
| **Target End Bib** | 200,000 |
| **OPAC Base URL** | [https://library.unikl.edu.my/](https://library.unikl.edu.my/) |
| **Subject Focus** | Technical engineering, aviation, automotive, marine, medical, and applied computing |

---

## Directory Structure

```text
unikl/
├── README.md                      # Institutional repository documentation
├── package.json                   # Node.js project specification & scripts
├── harvest/
│   └── inbox/unikl/             # Sealed MARCXML batch chunks and manifests
│       └── <run-id>-chunk-001/
│           ├── manifest.json      # Chunk SHA-256 manifest & metadata
│           ├── provenance.jsonl   # Record-level attribution and fetch logs
│           └── records/           # Batched MARC21 slim XML files
├── tools/
│   ├── harvesters/unikl/        # Automated OPAC crawler & XML converter
│   └── lib/                       # Supporting MARCXML and validation utilities
└── tests/
    └── harvester-unikl.test.js  # Autonomous test suite
```

---

## Usage

```bash
# Install dependencies
npm install

# Test run harvester (10 sample records)
npm run harvest:sample

# Run full collection sweep
npm run harvest:full

# Validate dataset integrity
npm run validate-inbox harvest/inbox/unikl/<chunk-directory>
```

---

## Attribution & License

Dataset harvested and preserved under open library metadata standards for educational, civic, and cooperative indexing. Attribution: **Universiti Kuala Lumpur Library (UNIKL)** & **Pustaka Terbuka**.
