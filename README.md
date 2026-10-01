# Repolex Knowledge Graph of block/fowlcon

RDF knowledge graph data for [block/fowlcon](https://github.com/block/fowlcon), parsed by [repolex](https://repolex.ai).

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
rlex download block/fowlcon
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── af5fa9ae07fd22595f72d6882c2c75fd0476eed4
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── af5fa9ae07fd22595f72d6882c2c75fd0476eed4.nq.gz
│   └── repolex
│       └── af5fa9ae07fd22595f72d6882c2c75fd0476eed4
│           └── chunk-001.nq.gz
├── blob
│   ├── 05df1ec6dc6fb01b36e439ea3b495cb3e9c25b79.nq.gz
│   ├── 0ba9db25329d0b336e39ca8cde8470c5b7bc45eb.nq.gz
│   ├── 181c02a03492c4975aa966903fb51491786052eb.nq.gz
│   ├── 1c6a04f5e4ded14c65bc591307abcb6516bbb07e.nq.gz
│   ├── 1d047d4ed8909f4d81fb105179bb24c4cac6d3db.nq.gz
│   ├── 236654adb4a0e2f75d4a9ab3d4ddf6bc346fdbcb.nq.gz
│   ├── 25f0bc5ed80683a81f46e6bfd1cf8ea0b56c6807.nq.gz
│   ├── 26d76c91c04936b571e8b21ad6ca3680110d52d0.nq.gz
│   ├── 2cbecdf8755196d982ecd604ca54ad77d2f7f9e9.nq.gz
│   ├── 2ec0cd414af876d1fa39a525c7037c23d7cd6913.nq.gz
│   ├── 34460e957148667d9c9cea5a87975f68c2092971.nq.gz
│   ├── 3897ebe985f7d0332ec028cc9060adb974b77e95.nq.gz
│   ├── 42e6273949733e7bbea143845c4814f84df90a81.nq.gz
│   ├── 43da18be5957f64f2c43b26676b79b4536932b9d.nq.gz
│   ├── 47dc3e3d863cfb5727b87d785d09abf9743c0a72.nq.gz
│   ├── 4cf522f21d03c6b4b300d7e448a4be318c14af4e.nq.gz
│   ├── 4eb644bbb9ca8cdbbd3a77cd9b93824dc74c3e81.nq.gz
│   ├── 508a14c6d38e63f2cd7d06df4646a7a6cdc64a42.nq.gz
│   ├── 513f52d308042aa57031f0ee1cbc456170f5ca4d.nq.gz
│   ├── 56583846f62a775f971967b52b5a1f03598b5e91.nq.gz
│   ├── 5734fa5faf7879529573aae33d6e94615739e1b5.nq.gz
│   ├── 59aef0d0099b794ab378336f83a7fe63a684b95f.nq.gz
│   ├── 5c73f16b8b86076fdd52032dd6a9aeacf1b09908.nq.gz
│   ├── 6bccf43368fd7c96d9c659562a5142b8b8cb98a1.nq.gz
│   ├── 6fbe32c67d2b34796792d0a033701d3d1b5be3e8.nq.gz
│   ├── 7e00828b07dda628765da67bc41304ccf080c582.nq.gz
│   ├── 862ee3c28647e7a58801a75236855c269c1448ae.nq.gz
│   ├── 8f8cee9aee59fa5d066609a06c8f359632d44e52.nq.gz
│   ├── 93fdad478706195d9fb7e8255b60988d49f7a1bc.nq.gz
│   ├── 9582fc588754f78d9875691a3bd5e674295436b3.nq.gz
│   ├── a106c8730d3dc3e1b18efa8581fa5e23daf7ab33.nq.gz
│   ├── a1542903508fd611b26da372a8ca5805dceb0652.nq.gz
│   ├── b3fb30857cdb988fc5eea491442988c80b33b2ea.nq.gz
│   ├── c15717bb34186bafcd708bc2810c395cba10143a.nq.gz
│   ├── c76f903ddee8aa385338403802aa0841aa2ac435.nq.gz
│   ├── e462859ffcbef418dfe8e27cd4130bc8cab7a5c4.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f0b6d0cafc251f092764e177d2b12b42489ff5da.nq.gz
│   ├── f7658d31e39d39a664c7b02aa39b97f30b2f86ef.nq.gz
│   └── fdaf05f97a4eb2faaa347319e1b0c31668503922.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── af5fa9ae07fd22595f72d6882c2c75fd0476eed4.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 49 files
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

[block/fowlcon](https://github.com/block/fowlcon)

---
*Parsed on 2026-10-01 by [repolex](https://repolex.ai)*
