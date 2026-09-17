# Repolex Knowledge Graph of python-hyper/brotlipy

RDF knowledge graph data for [python-hyper/brotlipy](https://github.com/python-hyper/brotlipy), parsed by [repolex](https://repolex.ai).

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
lexq download python-hyper/brotlipy
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3fd4d205e1a356c9b02faccfbe449e774537ddf2
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 3fd4d205e1a356c9b02faccfbe449e774537ddf2.nq.gz
│   └── repolex
│       └── 3fd4d205e1a356c9b02faccfbe449e774537ddf2
│           └── chunk-001.nq.gz
├── blob
│   ├── 011e6e16ca8858c5d4eb195c820f56f566e69dbd.nq.gz
│   ├── 07d2fbc51e7f1d7553dc78b77f4000cdcb28a7d5.nq.gz
│   ├── 115be2e9bf04c40d26e2920f1d03c5c947129f64.nq.gz
│   ├── 132a337341257483e366c666e352d3251ca23465.nq.gz
│   ├── 16761d05c8164eedeb2a4bf2b6d58197df4d9993.nq.gz
│   ├── 1eaa75460508ea5faac2a319ecad19b95f03a030.nq.gz
│   ├── 232a7308715dbb73b421e18d9ca5dd2bec94caa1.nq.gz
│   ├── 28988635d6e8986aaa433b8278fc3a14002c74fb.nq.gz
│   ├── 54d0380ff7c3113aff1755e310034e86fead549c.nq.gz
│   ├── 5a8f57469ea07f8ed433241fb008956f00b19709.nq.gz
│   ├── 6382f456c57685d05b897f043cb69454ce899347.nq.gz
│   ├── 73b2ef805576af97055a1be4d35b70fce37e7b12.nq.gz
│   ├── 742aa8473cdf8dede5a9c9486d1daaed1b6aedd5.nq.gz
│   ├── 76e7ef583065af5cb6277058c1da9aca678473ac.nq.gz
│   ├── 8aeadab4df4800df48774911890c91dbc1a8fcd6.nq.gz
│   ├── 8b62f4515e0bc10f6dfb61b5c008184afb8aaa37.nq.gz
│   ├── 8b7eaaf47d95871cbafa0579f4f445167ded54fd.nq.gz
│   ├── 8ee7ecce16077dd52a0b5690a9be38e2137272e6.nq.gz
│   ├── a355c5cf9abc0e783b74122527e1e1f28fb8233e.nq.gz
│   ├── a4805877961752621d26315d0467f8a258c63a98.nq.gz
│   ├── b2d33eefc2215d4505433ad801d39123c9b7a881.nq.gz
│   ├── d6466b602473a2683ccf84a9f6c6dce140a058e3.nq.gz
│   ├── dbf55a6b7ce955b58e44aaeef1b99c0ae0449095.nq.gz
│   ├── df6054424818f8c280b72c28b2bcae1e3e5085e4.nq.gz
│   ├── e1de0645c5eecd55a632548dd45b3caed8286a07.nq.gz
│   ├── e6601f455d7d582249cf2002a09195c6e6b0feac.nq.gz
│   ├── f3d1726551e27a84d78ba85d5159f18a6063bbc0.nq.gz
│   ├── f68542ec6f1e0cc5608142f075140af06a48be04.nq.gz
│   ├── faff4220d6c5b90cf05fa0dc792abfc2af3f9b16.nq.gz
│   └── fdfcbd67914d72d414e24a47439f157235954ae3.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 3fd4d205e1a356c9b02faccfbe449e774537ddf2.nq.gz
├── filetree
│   └── 3fd4d205e1a356c9b02faccfbe449e774537ddf2.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 40 files
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

[python-hyper/brotlipy](https://github.com/python-hyper/brotlipy)

---
*Parsed on 2026-09-17 by [repolex](https://repolex.ai)*
