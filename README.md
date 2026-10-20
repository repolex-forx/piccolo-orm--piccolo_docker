# Repolex Knowledge Graph of piccolo-orm/piccolo_docker

RDF knowledge graph data for [piccolo-orm/piccolo_docker](https://github.com/piccolo-orm/piccolo_docker), parsed by [repolex](https://repolex.ai).

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
rlex download piccolo-orm/piccolo_docker
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2bf2980c621cf02727c5049cb8d29a84b9dc18ef
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 2bf2980c621cf02727c5049cb8d29a84b9dc18ef
│           └── chunk-001.nq.gz
├── blob
│   ├── 06b99fec2d078e873174ea09c579792e11efdcb8.nq.gz
│   ├── 07b5989f7405cc3bd52fcd8cd26d7a6918c0e7fa.nq.gz
│   ├── 0d98e5f9edacd8456a420f2a9f68b077b3153553.nq.gz
│   ├── 1cdd7f6274b16b7f4e3a11606d07a1a2f48cddfd.nq.gz
│   ├── 26d0fbdf5fcbd7dcf221a5a7a4baeea76957fbda.nq.gz
│   ├── 3d08eb6bd77a5bc551f3a1e052e2bedfff2e6c3b.nq.gz
│   ├── 5b858340688701fa865f5bbeb035891bc6328c73.nq.gz
│   ├── 606b4dfb3d8b5e72d2c13f3091de9553511277a9.nq.gz
│   ├── 764134860402225f6b2fbb87ed8e355cad04b854.nq.gz
│   ├── 7da9d92b193c2a4c37e26ad6c7130e099d496a67.nq.gz
│   ├── 889098fe41ba055c56738341307a8aaa709c74e4.nq.gz
│   ├── 8b68bc165de3ace9a59f8919feddc6a87e3632ad.nq.gz
│   ├── 8dca64267c01b1c8c807901d76f52dcaff565f79.nq.gz
│   ├── a05c37860ea446f724f40004e1e5d58f7c02bfd2.nq.gz
│   ├── aad1da5a5521b47a4016f28675cd02005ee3d9f2.nq.gz
│   ├── b2c46fafdc5aaf9c560a008a094043147885ec3c.nq.gz
│   ├── b3c81e077a877f08bbc0c23f00e77f875638e513.nq.gz
│   ├── b5cc5fa888878a87db318803a6925083149c0a6f.nq.gz
│   ├── c41f6b7dc66595f540d8692eccf2fadcd2210e32.nq.gz
│   ├── d23b8d8e480308d3579937bcdc8a04f4d273e69d.nq.gz
│   ├── d59081604cc3e99c595f30732d3b883b32ca19e4.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f8ae6d00721737d967b4d49fa790e0db75f40c46.nq.gz
│   ├── fcbaf4e412585e69e1dd383984a535cf1794dc7d.nq.gz
│   ├── fe6b0a3dbb00ba7e9b05a6c139958021b485928a.nq.gz
│   └── ff69b9e7f8a9ed9c61dc6b986f4dcfcdb9cc113d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 2bf2980c621cf02727c5049cb8d29a84b9dc18ef.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 33 files
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

[piccolo-orm/piccolo_docker](https://github.com/piccolo-orm/piccolo_docker)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
