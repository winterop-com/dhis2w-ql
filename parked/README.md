# Parked callers of the engine

Everything in this directory drove `dhis2w_ql` from inside the `dhis2w` workspace and is kept
here, unchanged, for the day the query language returns as a `dhis2w` plugin pack:

- `plugins/v41`, `plugins/v42`, `plugins/v43`: the `d2w query` plugin, one copy per DHIS2 major
  (`cli.py`, `mcp.py`, `service.py`, `compiler.py`, `datasource.py`, `models.py`).
- `tui/`: the full-screen d2ql REPL behind `d2w query repl` (Textual).
- `tests/`: the plugin's test tree, parametrised over the three majors.
- `docs/`: the d2ql and d2path pages of the documentation site, plus the `dhis2w_ql` API page.
- `examples/`: the d2ql example corpus and the CLI, client and MCP example scripts.

The plugin imports `dhis2w_core.cli_output`, `dhis2w_core.v{N}.client_context` and the
`dhis2w_client.v{N}` accessors; a returning pack registers through the plugin entry point the
`dhis2w` repository documents at that time.
