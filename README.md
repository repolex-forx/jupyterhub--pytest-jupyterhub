# Repolex Knowledge Graph of jupyterhub/pytest-jupyterhub

RDF knowledge graph data for [jupyterhub/pytest-jupyterhub](https://github.com/jupyterhub/pytest-jupyterhub), parsed by [repolex](https://repolex.ai).

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
rlex download jupyterhub/pytest-jupyterhub
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0bc90cdd06c01c2a63ae56e36878ea25ce7642fd
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0bc90cdd06c01c2a63ae56e36878ea25ce7642fd
│           └── chunk-001.nq.gz
├── blob
│   ├── 00d658ad6bbad66309573e98d0a57d6e1c2af243.nq.gz
│   ├── 046891699e3cd25a7346fc799b6b80932165ee6f.nq.gz
│   ├── 0c4634c28c1e5cbc8060932731ae8f5af2be5d56.nq.gz
│   ├── 11b2611f23b256688d4f443e7f691bd2c3dc56d4.nq.gz
│   ├── 137479e21b25e02347c2ef877ef31abece9c7dbe.nq.gz
│   ├── 161bc16699bd812bb8246e83bb9690bfccaee975.nq.gz
│   ├── 1adfc160d9f1e71f522f6f9bc6ccfed68c806257.nq.gz
│   ├── 227ab731a5d1c3cf6c4f1e95fcd0a1d242b10061.nq.gz
│   ├── 26dacf5f8a899fb2567035f8fa982e3e03056cc1.nq.gz
│   ├── 3158d3c9ab86995c2eaed54284eacec4aff2112a.nq.gz
│   ├── 31b4a5d69fb6e7f8f07e5fc1b65172f6295daf07.nq.gz
│   ├── 31de969cd4acb716bc1964e7601c2cf78f9f6496.nq.gz
│   ├── 5362759277ee5529a679b23582eb434fb16d4cbf.nq.gz
│   ├── 5831f1b05372fdf122bb8a27ecdf06a5d4c51460.nq.gz
│   ├── 630c97519ff4b15790e230198c09ae277756932a.nq.gz
│   ├── 698ad83bf585ee8b8df0e7eeb52b70bc53555d73.nq.gz
│   ├── 6b193acae5901b1dc61ba53f08c65b92e5f8a620.nq.gz
│   ├── 7c424676304544e7d06f8b4e655e56fe0899e9a1.nq.gz
│   ├── 8ebb69b7e417a854fb779e85841482c8c6b818c6.nq.gz
│   ├── 92dd33a1a44470e1405a20c617694fd174086fcc.nq.gz
│   ├── a7a4e61b76ef38ddfc30a3e157aaae6674120bdf.nq.gz
│   ├── aaf05127ea65accfe630839316a6597cc0f57547.nq.gz
│   ├── b1f7f15ce6c4509b0ca9674775367dde943377f3.nq.gz
│   ├── b344c6a040f89866b827f28b5980dc35b51fcb53.nq.gz
│   ├── ba7204445bb565363f66e521c1c655b385f8795c.nq.gz
│   ├── c82e1dfc78032c2823da7a788697bb44c5de4a75.nq.gz
│   ├── d65de2f85fa12fbfe12fe35750fef3cb8cfcfca8.nq.gz
│   ├── d730c6f3f7ba2dea8eb69e50989fa713343e2ccd.nq.gz
│   ├── e0b85c1991fd87c128ef274d9d0e57c47328c74b.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e6f50bdae8bc4ac5cfaf25a914c3383334b6060d.nq.gz
│   ├── ffa2fe2d7fbe42e69ab0ee73b8833f2157d7c392.nq.gz
│   └── ffdf84e2314ca24a8b508642368dbba3bc61c7cc.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0bc90cdd06c01c2a63ae56e36878ea25ce7642fd.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 41 files
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

[jupyterhub/pytest-jupyterhub](https://github.com/jupyterhub/pytest-jupyterhub)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
