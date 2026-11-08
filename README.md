# Repolex Knowledge Graph of google-deepmind/agentic_ecology

RDF knowledge graph data for [google-deepmind/agentic_ecology](https://github.com/google-deepmind/agentic_ecology), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download google-deepmind/agentic_ecology
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 15d216543252d8b5e27b7c94c0f604485e60dbfe
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 15d216543252d8b5e27b7c94c0f604485e60dbfe
│           └── chunk-001.nq.gz
├── blob
│   ├── 0393da11295cece455d7aa6d0d3b666071e55cad.nq.gz
│   ├── 144098bbb820f9b49dfbbbe6a8f8f1a0e00bc0da.nq.gz
│   ├── 26d56dd29a068c365ad3d0bd0f6f0c39b0c581e6.nq.gz
│   ├── 28ca03c529a77e6b7312157c28905d30e0acef02.nq.gz
│   ├── 2c55a12a36fd4069204d84d822c027c1926ff099.nq.gz
│   ├── 2e64526e3993bb170072fe687eeda7b92638a682.nq.gz
│   ├── 507f9979a378adc6306aaae98dec0cdaadb1958f.nq.gz
│   ├── 6bd7d06dd72672de437739aea4bee645f4eca004.nq.gz
│   ├── 854eaa3068d3a0c7e347438628d965085b655889.nq.gz
│   ├── 8a6160a8729f15188d34217761cb4e7be27a287a.nq.gz
│   ├── 8fe94e1adc63ff77e132a1fa939daa643dece4c8.nq.gz
│   ├── 9042227f95044536a4644a09f82f43cc3694db52.nq.gz
│   ├── a7d7398a8c21d5c63f5655694e35ad06eee24a8e.nq.gz
│   ├── b5b4483bb583c5461c4a3ce529db7d5bd2236f73.nq.gz
│   ├── b98035a72cba8a9160f80f7bf9770e7147310a04.nq.gz
│   ├── bd5c6e6481647b10127eebc813ed52e4939a380d.nq.gz
│   ├── c2c9993191d848586c3088a3241ab3682c0eb285.nq.gz
│   ├── d51d8370ed3f454c9cac94a16051b7821c6acf8c.nq.gz
│   ├── d645695673349e3947e8e5ae42332d0ac3164cd7.nq.gz
│   ├── e0ce9729a8358a41e6457386b9e178ef07c1208d.nq.gz
│   ├── e3730d3889f7e1f7ebead0fd07b40e299be228ce.nq.gz
│   └── f3e22ef72f151a3b6721ff21a8cb57d84f808b23.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 15d216543252d8b5e27b7c94c0f604485e60dbfe.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 30 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[google-deepmind/agentic_ecology](https://github.com/google-deepmind/agentic_ecology)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
