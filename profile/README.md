# Ockham

**Agent-native infrastructure for financial and economic data analysis.**

Ockham builds the open data layer and agent framework that let an AI do real analytical work over financial and economic data. Connectors are typed Python functions with built-in provenance, a portable catalog makes thousands of data series discoverable through hybrid search, and an agent writes and runs its own code to turn questions into auditable datasets, charts, and reports.

The whole data stack is open source under Apache-2.0.

## The open stack

| Project | What it is | Install |
|---|---|---|
| [**parsimony**](https://github.com/ockham-sh/parsimony) | The kernel: typed data connectors and a portable hybrid-search catalog (BM25 + vectors) | `pip install parsimony-core` |
| [**parsimony-connectors**](https://github.com/ockham-sh/parsimony-connectors) | Ready-made connectors (FRED, SDMX, FMP, SEC EDGAR, BLS, EIA, central banks, and more), each its own package | `pip install parsimony-fred` |
| [**parsimony-agents**](https://github.com/ockham-sh/parsimony-agents) | An AI agent that writes and executes Python to analyze the data those connectors return | `pip install parsimony-agents` |

Full documentation lives at **[docs.parsimony.dev](https://docs.parsimony.dev)**.

## How it fits together

A connector is just an `async` Python function: you call it, and the framework returns a typed result carrying the data plus full provenance (source, parameters, fetch time). The catalog indexes thousands of those series so they can be found by keyword and by meaning at once. The agent sits on top: given a question, it finds the right data, writes Python against the typed results, runs it in a sandbox, and hands back artifacts you can trace end to end.

```
parsimony-core             typed connectors + a searchable catalog
  └── parsimony-connectors      the connectors themselves, one package each
        └── parsimony-agents         an agent that writes and runs code over the data
              └── Ockham Terminal        the workspace where an analyst puts it to work
```

## Ockham Terminal

[Ockham Terminal](https://ockham.sh) is the product built on this stack. It is a workspace, not a chatbot: an embedded coding agent does the analytical work while you direct and review it, and every dataset, chart, and report is saved with full lineage. The Terminal is open-core, an AGPL-3.0 core with a separately-licensed enterprise edition.

## Get started

```bash
pip install parsimony-agents
```

Bring your own connectors and your own model, then follow the [quickstart](https://docs.parsimony.dev).

## Community

- Each repository has its own `CONTRIBUTING.md` and good first issues.
- Ideas and questions are welcome in GitHub Discussions on any repo.
- For security reports, see a repository's `SECURITY.md` or email **security@ockham.sh**.

## License

The parsimony data stack (core, connectors, agents) is Apache-2.0. Ockham Terminal is open-core: an AGPL-3.0 core plus a separately-licensed enterprise edition.
