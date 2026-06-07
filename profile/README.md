<div align="center">

# Ockham

**Agent-native infrastructure for financial and economic data analysis.**

</div>

Ockham builds the open data layer and agent framework that let an AI do real analytical work over financial and economic data: typed connectors, a portable search catalog, and an agent that writes and runs its own code to turn questions into auditable datasets, charts, and reports.

## Projects

| Project | What it is | Install |
| --- | --- | --- |
| [**parsimony**](https://github.com/ockham-sh/parsimony) | The kernel: typed data connectors and a hybrid-search catalog | `pip install parsimony-core` |
| [**parsimony-connectors**](https://github.com/ockham-sh/parsimony-connectors) | Ready-made connectors (FRED, SDMX, FMP, SEC EDGAR, BLS, EIA, central banks, and more) | `pip install parsimony-fred` |
| [**parsimony-agents**](https://github.com/ockham-sh/parsimony-agents) | An AI agent that writes and runs Python to analyze the data | `pip install parsimony-agents` |
| **Ockham Terminal** _(coming soon)_ | The analyst workspace built on the stack, open-core (AGPL-3.0 + enterprise edition) | [ockham.sh](https://ockham.sh) |

Full documentation: [docs.parsimony.dev](https://docs.parsimony.dev)

## License

The parsimony data stack (core, connectors, agents) is **Apache-2.0**. Ockham Terminal is **open-core**: an AGPL-3.0 core plus a separately-licensed enterprise edition.
