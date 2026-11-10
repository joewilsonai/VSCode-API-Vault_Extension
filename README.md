<div align="center">

# API Vault

**Manage your API keys directly in VS Code: organized, searchable, one click to copy.**

A VS Code extension for developers who keep API keys in `.env` files, notes and chat messages to themselves. It gives them one side panel, with the values kept in VS Code's secret storage.

[Install from the VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=josephdavidwilsonjr.api-vault)

![The API Vault side panel, showing keys grouped into collapsible categories](api-vault-ui.png)

</div>

## Features

- **Side panel** in the activity bar (the API icon) with a form to add a key: name, value, optional category.
- **Categories** you create yourself, which collapse and expand. Drag a key to reorder it or to move it into another category, or pick the category from the key's dropdown.
- **Per key:** show or hide the value, copy it to the clipboard, or delete it (with a confirmation).
- **Search** that filters keys by name as you type.
- **Compact mode** for a denser list.

### Commands

Open the Command Palette and type "API Vault":

| Command | What it does |
|---|---|
| API Vault: Store Key | Asks for a name and a value (typed into a password box) and saves them |
| API Vault: Get Key | Pick a key and copy its value to the clipboard |
| API Vault: List Keys | Pick a key, then copy or delete it |
| API Vault: Create Category | Add a category |
| API Vault: Focus Search | Jump to the search box |
| API Vault: Toggle Compact Mode | Switch between the normal and compact list |
| API Vault: Populate Demo Data | Fill the vault with made-up sample keys and categories, for trying it out |

## How keys are stored

- **Values** go into VS Code's [SecretStorage](https://code.visualstudio.com/api/references/vscode-api#SecretStorage), which VS Code encrypts with your operating system's credential store. The extension does not write values anywhere else.
- **Key names, categories and view settings** are kept in VS Code's ordinary extension state (`globalState`), which is not encrypted. Do not put secrets in a key's name.
- Nothing is sent over the network.

## Install

**From the Marketplace:** open the Extensions view (`Cmd/Ctrl+Shift+X`), search for **API Vault**, and install the one published by `josephdavidwilsonjr`.

**From source** (VS Code 1.74 or newer):

```bash
git clone https://github.com/joewilsonai/VSCode-API-Vault_Extension
cd VSCode-API-Vault_Extension
npm ci
npx @vscode/vsce package --no-dependencies
code --install-extension api-vault-4.3.2.vsix
```

## Status

Last updated May 2026. Checked in November 2026: `npm ci`, `npm run compile` and `npm run lint` (warnings only) succeed, and `vsce package --no-dependencies` builds the `.vsix`. Without `--no-dependencies`, packaging failed in that check with "Extension entrypoint(s) missing". The Marketplace listing is version 4.0.3 (January 2025); this repository is at 4.3.2, which has not been published there.

## License

MIT. See [LICENSE](LICENSE).
