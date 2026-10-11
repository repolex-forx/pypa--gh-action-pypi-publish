# Repolex Knowledge Graph of pypa/gh-action-pypi-publish

RDF knowledge graph data for [pypa/gh-action-pypi-publish](https://github.com/pypa/gh-action-pypi-publish), parsed by [repolex](https://repolex.ai).

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
rlex download pypa/gh-action-pypi-publish
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c0d6f8e4af2ad8247a7da213b199ea78dac8395e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c0d6f8e4af2ad8247a7da213b199ea78dac8395e
│           └── chunk-001.nq.gz
├── blob
│   ├── 2124106330d3f124feb1bccde96486d38389fe87.nq.gz
│   ├── 2a29ff23bd4580ca2ca97ec5f8c58e279cf7a059.nq.gz
│   ├── 2f8bd1731d28329660c0530c7828f7d4d014cf4b.nq.gz
│   ├── 344404db570bf4873741072638d830954c7a2271.nq.gz
│   ├── 3dde2eaa4cfe6dee0045748b18c8db8a4fb2fca6.nq.gz
│   ├── 482e266a80292b84e9f12ab504943f2355e94416.nq.gz
│   ├── 48d54a348586258e8f38d1a7d303a7fda3e9d2f3.nq.gz
│   ├── 50e8c2955753415f5d573fd4464c469b7944606e.nq.gz
│   ├── 56323771f366b342bdbc23060bb1852a0f4db8d3.nq.gz
│   ├── 60061c347fd781884c524135e2ed6fd8c427aed3.nq.gz
│   ├── 793076e79e8487a0ccde07b2f077b8cbd5576a45.nq.gz
│   ├── 83f7d7c8f851c6cbc77ba1859e760e8cd00f5dff.nq.gz
│   ├── 894a44cc066a027465cd26d634948d56d13af9af.nq.gz
│   ├── 8bdb7e18bf29f3c04c4212ac17ae227777af59a2.nq.gz
│   ├── 92346bd1e3a55ccb0040640720af1018f71936ce.nq.gz
│   ├── 9a580ab394f8cc70179b133772e76c694dbe1a6c.nq.gz
│   ├── a1e048e6c8eb16d6d3d4196f373f09693de70379.nq.gz
│   ├── a29e3e70e4efeadf6e43665be9b88629cc70a5ff.nq.gz
│   ├── aba4b4ad6a99b1a2944db4ebf48fc3c81f548129.nq.gz
│   ├── ae6040561a8194ebfd860f6332e7881b494e17f3.nq.gz
│   ├── af5fe368e6986537109860542fc56f5a022de7da.nq.gz
│   ├── afe6c24dabeec67486595d491d07bcddb60e12fa.nq.gz
│   ├── c81d82c9f91a93f8b5efbde667d353ed32f1891a.nq.gz
│   ├── c89e1b012343b113b2eb5e1c4fee2e700b76b5db.nq.gz
│   ├── dd64f3d5ee6cdfcf3dc4f5bedef937bff4026dd9.nq.gz
│   ├── e0df184b50f56028527a25ed693f1e27ec6f2515.nq.gz
│   ├── f0b2c5066dd5e752990bc69b0109e84563bc8db1.nq.gz
│   ├── f33e325e73e0df19854a150a159573e322991a02.nq.gz
│   └── fd411b3233f8a2d35cae1922a893cd3f67ae7349.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c0d6f8e4af2ad8247a7da213b199ea78dac8395e.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 37 files
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

[pypa/gh-action-pypi-publish](https://github.com/pypa/gh-action-pypi-publish)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
