<div align="center">

# 🔒 API Vault

**Manage your API keys directly in VS Code — encrypted, organized, one-click access.**

API Vault stores your keys in the system keychain (macOS Keychain / Windows Credential Vault / Linux libsecret) and surfaces them in a clean side-panel UI so you stop pasting keys into Notes.app.

[![Marketplace](https://img.shields.io/badge/VS_Code-Marketplace-007ACC?logo=visualstudiocode)](https://marketplace.visualstudio.com)
[![License](https://img.shields.io/badge/License-MIT-blue)](#license)
[![Stars](https://img.shields.io/github/stars/joewilsonai/VSCode-API-Vault_Extension?style=social)](https://github.com/joewilsonai/VSCode-API-Vault_Extension/stargazers)

![API Vault UI](api-vault-ui.png)

</div>

---

## Why

You have 30 API keys across 12 services. They live in:

- A `.env` file you accidentally committed once
- Apple Notes
- A Google Doc called *"keys.doc"*
- Slack DMs to yourself
- Your password manager's "miscellaneous" folder

**API Vault gives you one place** — a VS Code side panel — that lives inside your editor and stores everything in your OS keychain.

## Features

### 🎯 Organized
Categorize keys however you want. Default categories:

- ☁️ Cloud Services (AWS, Azure, GCP)
- 💳 Payment APIs (Stripe, PayPal)
- 🔗 Social Media (Twitter, Facebook)
- 🤖 AI & ML (OpenAI, Anthropic, HuggingFace)
- 🛠️ Development Tools (GitHub, GitLab)

### 🔐 Encrypted by default
- Stored in the **system keychain** — macOS Keychain, Windows Credential Vault, Linux libsecret
- **Never plain-text on disk**
- **No cloud sync** — your keys stay on your machine

### ⚡ Fast
- **One-click copy** straight into your editor
- **Quick search** with `⌘/Ctrl+F`
- **Create categories** with `⌘/Ctrl+Shift+N`
- **Compact mode** with `⌘/Ctrl+Shift+C`
- **Drag-and-drop** keys between categories

## Install

### From the VS Code Marketplace

1. Open Extensions in VS Code (`⌘/Ctrl+Shift+X`)
2. Search for **API Vault**
3. Click Install

### From source

```bash
git clone https://github.com/joewilsonai/VSCode-API-Vault_Extension
cd VSCode-API-Vault_Extension
npm install
npm run package
code --install-extension api-vault-*.vsix
```

## Usage

1. Open the API Vault side panel (icon appears in the activity bar after install)
2. Click **+ New Key**
3. Enter name, value, and category
4. Click any key to copy — the key never leaves your keychain except into your clipboard

## License

MIT
