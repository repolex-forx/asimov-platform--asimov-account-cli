# Repolex Knowledge Graph of asimov-platform/asimov-account-cli

RDF knowledge graph data for [asimov-platform/asimov-account-cli](https://github.com/asimov-platform/asimov-account-cli), parsed by [repolex](https://repolex.ai).

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
lexq download asimov-platform/asimov-account-cli
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── blob
│   ├── 00164dc03be3777ec7436c4d8e7ebbafe379220d.nq.gz
│   ├── 0d29b413d3a30a3012cc627862195caea84ea5e1.nq.gz
│   ├── 0ebdd983de91f3febb62be0df97af3d50d8a3a03.nq.gz
│   ├── 1109dd81a65380c9ce2f9f7a6ba33ba54ab0908b.nq.gz
│   ├── 13edb27f8341a15f7ef6805243c5be8572913129.nq.gz
│   ├── 2391f73aa051d3804285ce744f2e9a1c7e08993d.nq.gz
│   ├── 340b16e489d45d8463c691e7b49fa8572a1df3e7.nq.gz
│   ├── 3a34e2964268e8e53840ede1eb1a4dfb3696e053.nq.gz
│   ├── 51e7bdc94e090c1e124270c5b99a3418c90a221e.nq.gz
│   ├── 70b50f72a723fd5825b898131b2db43e718d6b18.nq.gz
│   ├── 8b85e1998da7b980fd6e73025499443c58d9f113.nq.gz
│   ├── a718674ce58c2cb835775828c8a323d259c0848c.nq.gz
│   ├── af99d7b2bdc0c86ee2288a7743c4f39c977d436d.nq.gz
│   ├── c7504b17b600cacd0a72d17b05bb8dae214c4791.nq.gz
│   ├── cff6707c09c5a607a4353d841a4d4a61276813c7.nq.gz
│   ├── d2d774d685a805fac62723c16262a6ba9ded7549.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ec50a64ded33981836d5e4a10ec60f3501f1ce74.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   └── f3ea931bc2b4226212ac31c3c8af4663b9cf2944.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── a3f53eb9a6e28a877a893d0f1d79bef20e2f0ec5.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

8 directories, 27 files
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

[asimov-platform/asimov-account-cli](https://github.com/asimov-platform/asimov-account-cli)

---
*Parsed on 2026-04-03 by [repolex](https://repolex.ai)*
