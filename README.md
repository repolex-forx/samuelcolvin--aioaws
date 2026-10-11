# Repolex Knowledge Graph of samuelcolvin/aioaws

RDF knowledge graph data for [samuelcolvin/aioaws](https://github.com/samuelcolvin/aioaws), parsed by [repolex](https://repolex.ai).

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
rlex download samuelcolvin/aioaws
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d4141e30a11c2724558c330631de20ea02691f3d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d4141e30a11c2724558c330631de20ea02691f3d
│           └── chunk-001.nq.gz
├── blob
│   ├── 00732c7aa0c81655aac9600b274b5e84c4a00cb6.nq.gz
│   ├── 0363be88aae92aae5b3341c2756c89f1eccc4fb3.nq.gz
│   ├── 07489eecbb0c646fdbe5b9c75614e28500fe8c5b.nq.gz
│   ├── 09b392639cfcf91ae2303a725d16eda82010fb28.nq.gz
│   ├── 0a2afcc11e8f8932d31524a8e5d32711405cbde3.nq.gz
│   ├── 13142d98bef7b86613a9b4bc39cf04c14f17f772.nq.gz
│   ├── 1d7954840b4be278104a651473d5d42d57eab59e.nq.gz
│   ├── 3bbabc24594e8a986a62b590caf1748ae0178359.nq.gz
│   ├── 41f22d4621c9b9e08f188005d27c12859dfacaba.nq.gz
│   ├── 48e5584a85b5abed33590b8fa86b0eabcb95ca7b.nq.gz
│   ├── 5bdef56f5ec40195086064d18c006c7cabf95e90.nq.gz
│   ├── 5ef98c9e9c19e9e22acfd56e5f92cdc905fbe9fc.nq.gz
│   ├── 603812c0b1b0bc475e0b31dd62bd81431ad90bf3.nq.gz
│   ├── 62d6458f92d69e3295a7852442306f581cf66dc1.nq.gz
│   ├── 6d93fa74aad6640adaaf5b070bd7a5183fa7abd9.nq.gz
│   ├── 6f10b4c3f6b9a58af0e6b4b8d98c2e67dd3a36db.nq.gz
│   ├── 6fafa524ff1848b9e938f42837a526381e604e14.nq.gz
│   ├── 79ed476c3714ad4d551b084605332625f66fe40c.nq.gz
│   ├── 7dd041c25b2e3141eb4924c042a4588076411efc.nq.gz
│   ├── 7e1e7a310504cefe3bfd02fcc475001d5800d551.nq.gz
│   ├── 7e6ef6625e0351c24ca0f08e52d0d03eacef1ce1.nq.gz
│   ├── 89a3ff33d21ba52ad01ee0e479ea9a46d36863cd.nq.gz
│   ├── 89fb8b7d3c4017179a4e451ae6e9d7f360685f10.nq.gz
│   ├── 9eab37da21c8810e7d731772c5e85ecd23389f69.nq.gz
│   ├── a23c98b37f61935ddb970103ed2f3557f8417f70.nq.gz
│   ├── c34390b9d395ec942718dbc642a97d81b76e3110.nq.gz
│   ├── cefdcfac1650327df454af48658afc8ac5213e08.nq.gz
│   ├── d36312f43cca127c434ddfb0c82c717b982faf18.nq.gz
│   ├── d688d60a989bb6394f217d5076ad72e217f45db0.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e7d56d100c8c8d660de53f31ef45ab1453f87b52.nq.gz
│   └── fe43ba90d5187df7256cdda5bef401c3cb41b9a8.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d4141e30a11c2724558c330631de20ea02691f3d.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 40 files
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

[samuelcolvin/aioaws](https://github.com/samuelcolvin/aioaws)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
