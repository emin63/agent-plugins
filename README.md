# emin-shopper-plugins

A Claude Code plugin marketplace with vendored, reviewed plugins. Every
change is reviewed through a pull request before it lands on `main`.

| Plugin | What it does |
|--------|--------------|
| [pyright-lsp](plugins/pyright-lsp) | Pyright language server for Python |

## Use

```sh
claude plugin marketplace add emin-shopper/agent-plugins
claude plugin install pyright-lsp@emin-shopper-plugins
```

Third-party marketplaces do not auto-update by default. To pull reviewed
changes, run `claude plugin marketplace update emin-shopper-plugins`.
