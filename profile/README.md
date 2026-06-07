<div align="center">

# Ockham

### Agent-native infrastructure for financial and economic data analysis

Typed data connectors, a portable search catalog, and an agent that writes and runs its own code,<br/>
so AI can do real analytical work over financial and economic data.

[![Docs](https://img.shields.io/badge/docs-parsimony.dev-4c6ef5?style=flat-square&logo=readthedocs&logoColor=white)](https://docs.parsimony.dev)
[![PyPI](https://img.shields.io/pypi/v/parsimony-core?style=flat-square&label=parsimony-core&color=4c6ef5)](https://pypi.org/project/parsimony-core/)
[![Data stack license](https://img.shields.io/badge/data%20stack-Apache--2.0-4c6ef5?style=flat-square)](https://www.apache.org/licenses/LICENSE-2.0)
[![Python](https://img.shields.io/badge/python-3.11%2B-4c6ef5?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)

</div>

## How it fits together

```mermaid
flowchart TD
    core["parsimony-core<br/><br/>typed connectors + searchable catalog"]
    conn["parsimony-connectors<br/><br/>one package per data source"]
    agents["parsimony-agents<br/><br/>an agent that writes and runs code over the data"]
    term["Ockham Terminal<br/><br/>the analyst workspace · coming soon"]

    core --> conn --> agents --> term

    classDef open fill:#eef2ff,stroke:#4c6ef5,stroke-width:1.5px,color:#1e293b;
    classDef soon fill:#f1f5f9,stroke:#94a3b8,stroke-width:1.5px,color:#64748b,stroke-dasharray:5 4;
    class core,conn,agents open;
    class term soon;
```

A connector is just an `async` Python function that returns a typed result with full provenance. The catalog makes thousands of series discoverable by keyword and by meaning at once. The agent finds the right data, writes Python against the typed results, runs it in a sandbox, and returns datasets, charts, and reports you can trace end to end.

## Projects

<table>
<tr>
<td width="50%" valign="top">
<h3><a href="https://github.com/ockham-sh/parsimony">parsimony</a></h3>
<p>The kernel: typed data connectors and a portable hybrid-search catalog (BM25 + vectors).</p>
<p>
<a href="https://pypi.org/project/parsimony-core/"><img src="https://img.shields.io/pypi/v/parsimony-core?style=flat-square&label=PyPI&color=4c6ef5" alt="PyPI" /></a>
<img src="https://img.shields.io/github/stars/ockham-sh/parsimony?style=flat-square&color=4c6ef5&label=stars" alt="Stars" />
<img src="https://img.shields.io/github/license/ockham-sh/parsimony?style=flat-square&color=4c6ef5" alt="License" />
</p>
<p><code>pip install parsimony-core</code></p>
</td>
<td width="50%" valign="top">
<h3><a href="https://github.com/ockham-sh/parsimony-connectors">parsimony-connectors</a></h3>
<p>Ready-made connectors: FRED, SDMX, FMP, SEC EDGAR, BLS, EIA, central banks, and more. Each ships as its own package.</p>
<p>
<img src="https://img.shields.io/badge/PyPI-per--package-4c6ef5?style=flat-square" alt="PyPI per package" />
<img src="https://img.shields.io/github/stars/ockham-sh/parsimony-connectors?style=flat-square&color=4c6ef5&label=stars" alt="Stars" />
<img src="https://img.shields.io/github/license/ockham-sh/parsimony-connectors?style=flat-square&color=4c6ef5" alt="License" />
</p>
<p><code>pip install parsimony-fred</code></p>
</td>
</tr>
<tr>
<td width="50%" valign="top">
<h3><a href="https://github.com/ockham-sh/parsimony-agents">parsimony-agents</a></h3>
<p>An AI agent that writes and executes Python to analyze the data those connectors return.</p>
<p>
<a href="https://pypi.org/project/parsimony-agents/"><img src="https://img.shields.io/pypi/v/parsimony-agents?style=flat-square&label=PyPI&color=4c6ef5" alt="PyPI" /></a>
<img src="https://img.shields.io/github/stars/ockham-sh/parsimony-agents?style=flat-square&color=4c6ef5&label=stars" alt="Stars" />
<img src="https://img.shields.io/github/license/ockham-sh/parsimony-agents?style=flat-square&color=4c6ef5" alt="License" />
</p>
<p><code>pip install parsimony-agents</code></p>
</td>
<td width="50%" valign="top">
<h3>Ockham Terminal &nbsp;<img src="https://img.shields.io/badge/coming_soon-64748b?style=flat-square" alt="coming soon" /></h3>
<p>The analyst workspace built on the stack: an embedded coding agent does the work while you direct and review, with every dataset, chart, and report saved with full lineage.</p>
<p>
<img src="https://img.shields.io/badge/model-open--core-64748b?style=flat-square" alt="open-core" />
<img src="https://img.shields.io/badge/core-AGPL--3.0-64748b?style=flat-square" alt="AGPL-3.0 core" />
</p>
<p><a href="https://ockham.sh">ockham.sh →</a></p>
</td>
</tr>
</table>

## Quickstart

```bash
pip install parsimony-agents
```

Bring your own connectors and your own model, then follow the [quickstart](https://docs.parsimony.dev).

## Community

- **Docs** &middot; [docs.parsimony.dev](https://docs.parsimony.dev)
- **Discussions & issues** &middot; on each repository above
- **Security** &middot; [security policy](https://github.com/ockham-sh/.github/blob/main/SECURITY.md) or security@ockham.sh

## License

The parsimony data stack (core, connectors, agents) is **Apache-2.0**. Ockham Terminal is **open-core**: an AGPL-3.0 core plus a separately-licensed enterprise edition.
