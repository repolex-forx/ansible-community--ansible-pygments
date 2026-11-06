# Repolex Knowledge Graph of ansible-community/ansible-pygments

RDF knowledge graph data for [ansible-community/ansible-pygments](https://github.com/ansible-community/ansible-pygments), parsed by [repolex](https://repolex.ai).

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
rlex download ansible-community/ansible-pygments
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 1a68878ae8a70bc69d02cfdd0b2f7fb963c79e54
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 1a68878ae8a70bc69d02cfdd0b2f7fb963c79e54
│           └── chunk-001.nq.gz
├── blob
│   ├── 0204a833e9b9eaa33d90d02c88e0e683ecd2fca7.nq.gz
│   ├── 093cede2b964d1a01336a8a89af71b054dcec45e.nq.gz
│   ├── 114ca05d0e9681f1b71412081e4a054cec80a6cd.nq.gz
│   ├── 126e972691421fb17b438badd04b0fc5c5b85f9b.nq.gz
│   ├── 2a25a43db38ef418b32036d94def130e8dba1d1a.nq.gz
│   ├── 4abacdef4d408ebd3b98ef53bce93ae6f29b8dfd.nq.gz
│   ├── 5ea85041080b0080aeeaacb39ae7df783e1be1f8.nq.gz
│   ├── 6ef52ad7c232196d5ae4ecbc3f94e9f7373ff9e2.nq.gz
│   ├── 71966d22ab8fe97bfc22b9ba11116aea4d3b82b7.nq.gz
│   ├── 7a28fa9b19b678d01779c0fa8953e460dfd07f13.nq.gz
│   ├── 7b90c41c2be29aa5db1439345f4d6028e439a4de.nq.gz
│   ├── 81e1c6780dcf0626ba5c77cb9bad8176da02edb9.nq.gz
│   ├── 86d422af79db46a967d239abce6aee30b17d4f28.nq.gz
│   ├── a306fc9f2b0f1565b7cdcaf5216a91e89fe4dd16.nq.gz
│   ├── a842a7c76ed03018048d65ec99eff6fc1979103b.nq.gz
│   ├── a91bc29c4f8e62de40a66fefe584686a214b793d.nq.gz
│   ├── ae827351c9e22bdabce9a93c8d81f46285a503f2.nq.gz
│   ├── d63d974f3174c13c816c1f7f268a122a5d42e514.nq.gz
│   ├── d93cb98244d6bf47007b06dc937104a61dc050ec.nq.gz
│   ├── dccae4597d7ac5c77174f4e868d6a9080f07db0f.nq.gz
│   ├── f15276aff3b84b08968192ba5558162718ed2e4d.nq.gz
│   ├── f8007f64a52d7eed9e3a3baaeb92aba69484e7d8.nq.gz
│   └── faafb993f0de60428670d919d9330d4942ea6f43.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 1a68878ae8a70bc69d02cfdd0b2f7fb963c79e54.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 31 files
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

[ansible-community/ansible-pygments](https://github.com/ansible-community/ansible-pygments)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
