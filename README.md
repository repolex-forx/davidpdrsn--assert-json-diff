# Repolex Knowledge Graph of davidpdrsn/assert-json-diff

RDF knowledge graph data for [davidpdrsn/assert-json-diff](https://github.com/davidpdrsn/assert-json-diff), parsed by [repolex](https://repolex.ai).

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
rlex download davidpdrsn/assert-json-diff
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── bca0d2c590808274298d939e0533da79cd09076d
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── bca0d2c590808274298d939e0533da79cd09076d.nq.gz
│   └── repolex
│       └── bca0d2c590808274298d939e0533da79cd09076d
│           └── chunk-001.nq.gz
├── blob
│   ├── 1bbe8ee11073c9c819df08b5a38b0f7c525715db.nq.gz
│   ├── 286e99e846f475e13af00191f170a792e745baef.nq.gz
│   ├── 411eea548ea690cf9b54c912e7c27003d96c0b62.nq.gz
│   ├── 498dd6f621849ea249865d1b033cfea270cd170c.nq.gz
│   ├── 693699042b1a8ccf697636d3cd34b200f3a8278b.nq.gz
│   ├── 6abc94e7262f3ce92eb46bcdbfea374d232a8965.nq.gz
│   ├── 7abf1c78f12bca968c8c1937bc03971e79e900e5.nq.gz
│   ├── 7b1c4d56adf3062af8556bb31d2ed69639becfef.nq.gz
│   ├── 961b34910885366271e298ce13656c1e501ed282.nq.gz
│   ├── d824be41db0cda4ccb58a50289f11c1ddb6d8782.nq.gz
│   ├── daeabc3df95dc4c81dc1902f6107a0d6d2f8d1e8.nq.gz
│   └── f73cdc8bb6a023aec8469aa0a086f9b84d1d729c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── bca0d2c590808274298d939e0533da79cd09076d.nq.gz
├── filetree
│   └── bca0d2c590808274298d939e0533da79cd09076d.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 22 files
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

[davidpdrsn/assert-json-diff](https://github.com/davidpdrsn/assert-json-diff)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
