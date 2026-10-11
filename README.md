# Repolex Knowledge Graph of agronholm/ircproto

RDF knowledge graph data for [agronholm/ircproto](https://github.com/agronholm/ircproto), parsed by [repolex](https://repolex.ai).

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
rlex download agronholm/ircproto
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 7993857e0f475f9fe8484bc669906cf1d6add0dd
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 7993857e0f475f9fe8484bc669906cf1d6add0dd
│           └── chunk-001.nq.gz
├── blob
│   ├── 02737fb4c218cf4c3abffc86fe18e41c8cb3651c.nq.gz
│   ├── 067698fa627e6669579f4ca32be31fe3f95c98fd.nq.gz
│   ├── 07806f8af9dd3253ebdb5710b67e73124aea4941.nq.gz
│   ├── 195a044860e795f1af1452bd1c6998ae4885eee0.nq.gz
│   ├── 1c889b90ad549fe8b4eda6b101146661a0f9a487.nq.gz
│   ├── 21d2b896b7e0405e2c40f6a3725014676788444c.nq.gz
│   ├── 2b90e0616134dc78c8383fa7338bfb5db6e1a0c8.nq.gz
│   ├── 2e554a1920229c61d7b4565fdd16e0fcdb0789b6.nq.gz
│   ├── 36cd8e1acd59e863fe9c36307f53f3b8ed333d16.nq.gz
│   ├── 38f0666c157e3a9943d2548b066f54dd0443cf8d.nq.gz
│   ├── 4384d0efa60d02781171dd9c2e27453a64b65e05.nq.gz
│   ├── 4be48e4bd8ce5aec51ef5fe9fb7b9243bec5ea30.nq.gz
│   ├── 4f3d05de386ea34f146c072cc8d0467b4ae73b95.nq.gz
│   ├── 5d0714c5413a93bab59dddf91425b45815062ef6.nq.gz
│   ├── 6a706e4be3a15d9d1f2cb6ba76bbb1292f01a044.nq.gz
│   ├── 705730881506d287298d2e12c9a5d0646a92e3c5.nq.gz
│   ├── a1d925280c564f928d447fb232a4caedc50e5f8d.nq.gz
│   ├── adaa6030692c60e8824e9924b4141d7e742055ab.nq.gz
│   ├── afd187c48337ba01cc0d5f4433584c2492514e86.nq.gz
│   ├── b2db62335d7aa79a29c1f20b02e0c9f9e36e840b.nq.gz
│   ├── c9b3364ad38db0f20c33093dbf401886f9afd539.nq.gz
│   ├── ce61c472fc4ad10840f5b6f042932187ec1fee01.nq.gz
│   ├── cf24fa5d2612fad5278cf75c45cff2491905336a.nq.gz
│   ├── d3bf1b1a7290256fe2350ab1a06dc83de5fbe135.nq.gz
│   ├── daaa003a6811c6c4617d21c3eb866a102e761457.nq.gz
│   ├── e453324c3a6c4ad8d8a02e79ac40b50cabcab09d.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f0b9380e71d1f266811ec7cdfd0c97a92736b85b.nq.gz
│   └── fd4911bfa5ba0d396646a7ffc52572f60ca17949.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 7993857e0f475f9fe8484bc669906cf1d6add0dd.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 36 files
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

[agronholm/ircproto](https://github.com/agronholm/ircproto)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
