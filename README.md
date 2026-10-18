# Repolex Knowledge Graph of serge-sans-paille/gast

RDF knowledge graph data for [serge-sans-paille/gast](https://github.com/serge-sans-paille/gast), parsed by [repolex](https://repolex.ai).

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
rlex download serge-sans-paille/gast
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── df3a87952aae7ac92ea06c289e05cc3698d3eb3c
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── df3a87952aae7ac92ea06c289e05cc3698d3eb3c
│           └── chunk-001.nq.gz
├── blob
│   ├── 08f5bd310edb552099c894ea3d5c6d936ecb1366.nq.gz
│   ├── 0e9f10cd120c8be5a157acf78c92e992f2f75a0f.nq.gz
│   ├── 2915e056c19fc7abc24d686819cd7ef7f9d3415b.nq.gz
│   ├── 317cc08453d2373131b34ce0a10ed9636ce4d732.nq.gz
│   ├── 43cc3f643ec32b755208326c1d7bcd19e79909c5.nq.gz
│   ├── 451fe5b0eb6170c999074499a3a64a9712c2a8fe.nq.gz
│   ├── 563733b4b9d9a6793c544590ac42642ba05d9c34.nq.gz
│   ├── 5a71b7bcb21ff978724d3388e17452dd0cfbf932.nq.gz
│   ├── 5acd69e0d01baa430a7258cc7ee5287ae936c7f6.nq.gz
│   ├── 60a184b8a91afbe29835f48570a6d7258fd5627d.nq.gz
│   ├── 6d6c27fb17021c7c8b1ccc3f7ecb88a72167680c.nq.gz
│   ├── 867208672f8417782fc3c4b059f1f22fa09aa1d0.nq.gz
│   ├── 8955d3fbcfde6349723fba66cfe586df68839633.nq.gz
│   ├── 8de66c693fe55d4ebfa8f920e1c7d4672e8a3d2d.nq.gz
│   ├── 98eb1b76480012ba843699d862f02a0bd5495fe0.nq.gz
│   ├── a204a60704a30ed618b8e3569ce04887e7a4f15f.nq.gz
│   ├── a51835487b56c9024d350000f88dc57119733922.nq.gz
│   ├── a71c5c7f113e884f246252532ba9346cca77973c.nq.gz
│   ├── c621b672efad0e26c4c7a2856171210d214078d2.nq.gz
│   ├── c8ebb55b7fe465dd5d733c5efd456418db21d216.nq.gz
│   ├── c8f89ef3f17905e00019b19fd4488213399344cf.nq.gz
│   ├── c92a079442d77acf2b3a60579cd113088808eb5c.nq.gz
│   ├── cc8fa42364e3199e1d448ab43f23ff715b4c9633.nq.gz
│   ├── d2bd946cc448051c8c7604bf3caf3125683fd41f.nq.gz
│   ├── f5272a5bcc463a611449441e51c2e1983f789566.nq.gz
│   └── f8afc7b2933e23c0698fb98f466f0f22b7a58ccf.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── df3a87952aae7ac92ea06c289e05cc3698d3eb3c.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 34 files
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

[serge-sans-paille/gast](https://github.com/serge-sans-paille/gast)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
