# Repolex Knowledge Graph of mattstyles/grunt-banner

RDF knowledge graph data for [mattstyles/grunt-banner](https://github.com/mattstyles/grunt-banner), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download mattstyles/grunt-banner
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── fceed8c9860602c8020053e7185cf572efc0fe9f
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── fceed8c9860602c8020053e7185cf572efc0fe9f.nq.gz
│   └── repolex
│       └── fceed8c9860602c8020053e7185cf572efc0fe9f
│           └── chunk-001.nq.gz
├── blob
│   ├── 0d4e57507392f69b5309684759c4e18208b700e4.nq.gz
│   ├── 4070b48204e300685b591f20f06c49f55c34bf0d.nq.gz
│   ├── 6b4c1a9b135644073f3fd34a71452a0b1fe95abc.nq.gz
│   ├── 8eae9a561a0faeb579148a64570032d4047f9f6d.nq.gz
│   ├── 9538fc81864bb8ae91206cc55918f6a294ef70e0.nq.gz
│   ├── a90cbd741f6e6256b1c5b99eca2985534e105d35.nq.gz
│   ├── b2e215152a6f5111d502090fd616e98fe4c9e55f.nq.gz
│   ├── db9b2816794b4c2401c792c2e3db4a70d7547aec.nq.gz
│   ├── e28e1421cb168d97ca6ce3e7c8b9b214a11accef.nq.gz
│   ├── e521435e1f9b64717b9872376961232cf646f844.nq.gz
│   └── e6a931710036517bbcccb2a8f930bd4f7231369c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── fceed8c9860602c8020053e7185cf572efc0fe9f.nq.gz
├── filetree
│   └── fceed8c9860602c8020053e7185cf572efc0fe9f.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 21 files
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

## Source repository

[mattstyles/grunt-banner](https://github.com/mattstyles/grunt-banner)

---
*Parsed on 2026-04-18 by [repolex](https://repolex.ai)*
