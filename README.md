# Repolex Knowledge Graph of Pylons/translationstring

RDF knowledge graph data for [Pylons/translationstring](https://github.com/Pylons/translationstring), parsed by [repolex](https://repolex.ai).

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
rlex download Pylons/translationstring
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a8d0268000e51833650e82a87f065d0e629f3998
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── a8d0268000e51833650e82a87f065d0e629f3998
│           └── chunk-001.nq.gz
├── blob
│   ├── 00a3d6bcc366d65293f8b86b070bd04b5569406b.nq.gz
│   ├── 08bbdc70e0533d73aea4dd88e0bf508a57b327f5.nq.gz
│   ├── 11d9492e4305bb5d0f1ac1b86189a9a08797e475.nq.gz
│   ├── 12532e20e04113f97a677dcb72851e74f0b0d6f5.nq.gz
│   ├── 142b6ca357fee89f09803fc9ad7ff676500c37cf.nq.gz
│   ├── 17f83997702e2494159c91f053e1804c20b93273.nq.gz
│   ├── 1a2f4c80edfba0af60802ce3ce248b2f8c801129.nq.gz
│   ├── 2a5b7be49791ca98ae685704405b41873df6ff40.nq.gz
│   ├── 2c9d9b3badb72723385229b977ec81b016223bc2.nq.gz
│   ├── 2ce325e4b2b4485e78feaec8351ecf383d13b6c7.nq.gz
│   ├── 3946ef8d37a5770894ff43e3dbdb5d8ab4e587fd.nq.gz
│   ├── 40c420bba19aa08a0f43c83a2e320588f2b7e313.nq.gz
│   ├── 5050fb5d0f89b80328a85c0e74d09c162b4e14f5.nq.gz
│   ├── 53549dc44ff4cc0c71bf04debb8f9244f01b0f72.nq.gz
│   ├── 596270b527e35bc59d6d8530ff80613e6b2f5f72.nq.gz
│   ├── 5bb534f795ae0f566ba9f57c31944d8c6f45284c.nq.gz
│   ├── 5c29407fdaa070f082f62450d2b73dfe8ab7cfe6.nq.gz
│   ├── 69fa449dd96e2405945b2e4cff2fd0ab8b102097.nq.gz
│   ├── 76874976311bc3718b3345bea9aac3f0c06a04d7.nq.gz
│   ├── 79da996d72e8383db37bf78ee270bba16a1c4f60.nq.gz
│   ├── 8f4a5b958d8ed6c912869808ee8ae297d500af43.nq.gz
│   ├── 9b49b5e9f1ac0dea62a417d00bf5618e05072126.nq.gz
│   ├── a38c843ef709f8691f8027bdef1bf1a2dceff6b3.nq.gz
│   ├── bbeb77280e3697c57dce5122e997565d828a7798.nq.gz
│   ├── c21e5aa8a410a7fae8942ea5716f697424c4465f.nq.gz
│   ├── c40fbc2e4dc72893f0c790dc821f1d1cf77f1d49.nq.gz
│   ├── e11be66617cab4bfb4d48ce11539e260ac232275.nq.gz
│   ├── e392c5791b5951145fb1f87ea8afec375a7cf55f.nq.gz
│   ├── e7f8b0558ca4b968c0954984f90fd13a5164c3a3.nq.gz
│   └── fe247b0c983056b2fe0de4d039e80e4029e2df87.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── a8d0268000e51833650e82a87f065d0e629f3998.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 38 files
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

[Pylons/translationstring](https://github.com/Pylons/translationstring)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
