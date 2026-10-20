# Repolex Knowledge Graph of jaraco/jaraco.ui

RDF knowledge graph data for [jaraco/jaraco.ui](https://github.com/jaraco/jaraco.ui), parsed by [repolex](https://repolex.ai).

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
rlex download jaraco/jaraco.ui
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3e251f9967a550a119925c25649e5c40ac917c9d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 3e251f9967a550a119925c25649e5c40ac917c9d
│           └── chunk-001.nq.gz
├── blob
│   ├── 05ecf2c741756cd37dfa3ee65316e641091d784c.nq.gz
│   ├── 0ceda86edc2f76f33116f7b333d174a2b6ef0994.nq.gz
│   ├── 10d412f406891b9683f832fcbc134c9bdf4f916e.nq.gz
│   ├── 1e78495252763cf558f2a6c092628cfe7f3275dc.nq.gz
│   ├── 1f2aa7533b0423a8eb943f6f4ec02498e39581a0.nq.gz
│   ├── 240329c3604d8ead4c10aa8c88352caa8e4ce7b2.nq.gz
│   ├── 2428e2eb11e6db1886597c744a670c137edf1ee9.nq.gz
│   ├── 2e3f4dd791a6372b427d618eb0baa8c4dc58e5f0.nq.gz
│   ├── 304196f81e11a168c9894f966e4a617ebf4ed53c.nq.gz
│   ├── 47870ecc52b6be865f9a6e6cbb4c3cd20b2192a0.nq.gz
│   ├── 4dcdff1d9f54ada980e106547b1332cd46950bd4.nq.gz
│   ├── 5270c1447ece6c2ffa135c9f8c740b838cd14bd3.nq.gz
│   ├── 5376a4b4c0e7a551feaa55cf081554bc9944f744.nq.gz
│   ├── 54c9000ec94341dd65c2053251b85b124017b9b5.nq.gz
│   ├── 54cc8303b22089e12053e552d4e6cb852a865b8a.nq.gz
│   ├── 577e87a793a20e413f7321f4f17ec1eba2ea1962.nq.gz
│   ├── 5bdc232005af9be104a00437ae9bc64417a4c1cc.nq.gz
│   ├── 700235be57c1b2872455c0be5333f59cf568e252.nq.gz
│   ├── 724370638fc188317bbc7dc868f1a571995fd796.nq.gz
│   ├── 9a0f3bce1395ae3819030b822e5d9076c85068ea.nq.gz
│   ├── b971c9b72038715c594c17e3f66f27865d969c70.nq.gz
│   ├── d9ad963c37fa5632fa472b54f36b7127147720e3.nq.gz
│   ├── d9ce81b22539327fe7d26d990fcc450c586e4b84.nq.gz
│   ├── da24a7ba830cf335efa221108c0c363c87761d3b.nq.gz
│   ├── e05a3d4a2ab888e32952006d8cd380864368db5f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── efa2d23bcd60d728b6a56fa3eece3978f707763a.nq.gz
│   └── efcb8cbc2043faa7caf4f92fc7488bd6914c934c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 3e251f9967a550a119925c25649e5c40ac917c9d.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 36 files
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

[jaraco/jaraco.ui](https://github.com/jaraco/jaraco.ui)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
