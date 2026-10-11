# Repolex Knowledge Graph of tox-dev/action-pre-commit-uv

RDF knowledge graph data for [tox-dev/action-pre-commit-uv](https://github.com/tox-dev/action-pre-commit-uv), parsed by [repolex](https://repolex.ai).

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
rlex download tox-dev/action-pre-commit-uv
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 4de52c139ed1a6963bcc4c30042c4ef9d75d8b11
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 4de52c139ed1a6963bcc4c30042c4ef9d75d8b11
│           └── chunk-001.nq.gz
├── blob
│   ├── 0198f8af4e57f96b1ca7b4b4884f762e5e7d4196.nq.gz
│   ├── 0439c9183a133860befcc2585dd27c9a2c74b83b.nq.gz
│   ├── 43ff51ca96b3a2d2bd542fa1f434a962d27a3d9b.nq.gz
│   ├── 4cc50cdd11101fd69ff9ebaa447db0ac2998e02a.nq.gz
│   ├── 5a4128de7f16972c216a66cf8d9b13716c1b6111.nq.gz
│   ├── 7525626dbb20b73b6a9e04ac123acd03f6ad4068.nq.gz
│   ├── 9d1e0987bfc323000b570d680343f00c53ddbc3d.nq.gz
│   ├── ae419c100b25005bd082785a7709b42a9e0300ba.nq.gz
│   ├── d75f3352df889a351de19853d04ba0efc75691db.nq.gz
│   └── fc0406ff06dd9076662cdeceedcb29c997256934.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 4de52c139ed1a6963bcc4c30042c4ef9d75d8b11.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 18 files
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

[tox-dev/action-pre-commit-uv](https://github.com/tox-dev/action-pre-commit-uv)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
