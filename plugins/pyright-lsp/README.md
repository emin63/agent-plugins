# pyright-lsp (vendored)

Connects Claude Code to the Pyright language server for `.py` and `.pyi`
files. This plugin contains only configuration. It does not include
Pyright, and it has no hooks, MCP servers, skills, commands or agents.

## Provenance

Vendored from `plugins/pyright-lsp` in
[anthropics/claude-plugins-official](https://github.com/anthropics/claude-plugins-official/tree/aecd4c852f10b466245f18383fa6aad8c0b10d57/plugins/pyright-lsp)
at commit `aecd4c852f10b466245f18383fa6aad8c0b10d57`, which is
Apache-2.0 licensed (see `LICENSE`).

Changes from upstream:

- The `lspServers` config moved from the upstream marketplace entry
  into `.claude-plugin/plugin.json`.
- `command` is the absolute path `/usr/local/bin/pyright-langserver`
  instead of a `PATH` lookup, so nothing earlier on `PATH` can stand
  in for the server.

## Requirements

Pyright from npm (`npm install -g pyright@<pinned version>`), which
installs `/usr/local/bin/pyright-langserver`. Do not use the PyPI
`pyright` package: it is a third-party wrapper that downloads Pyright
from npm at run time.
