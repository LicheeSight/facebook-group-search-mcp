# Facebook Group Search MCP Server

[![Smithery](https://smithery.ai/badge/@licheesight/agentbridge)](https://smithery.ai/server/@licheesight/agentbridge)
[![npm version](https://img.shields.io/npm/v/@licheesight/agentbridge.svg?color=blue)](https://www.npmjs.com/package/@licheesight/agentbridge)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![MCP](https://img.shields.io/badge/MCP-Model%20Context%20Protocol-orange.svg)](https://modelcontextprotocol.io)

Search and extract discussions, posts, and comments across joined Facebook Groups directly from your AI agents (**Cursor**, **Claude Desktop**, **Windsurf**, and **VS Code Copilot**) using your signed-in browser session.

---

## ⚡ 1-Click Quick Install (Smithery)

You can automatically install and configure this MCP server using the [Smithery CLI](https://smithery.ai):

### For Claude Desktop
```bash
npx -y @smithery/cli install @licheesight/agentbridge --client claude
```

### For Cursor
```bash
npx -y @smithery/cli install @licheesight/agentbridge --client cursor
```

### For Windsurf / VS Code
```bash
npx -y @smithery/cli install @licheesight/agentbridge --client vscode
```

---

## 🛠️ Manual Configuration

If you prefer to configure manually, add the following to your AI client's MCP configuration file (e.g., `claude_desktop_config.json` or Cursor Settings):

```json
{
  "mcpServers": {
    "facebook-group-search": {
      "command": "npx",
      "args": [
        "-y",
        "@licheesight/agentbridge"
      ]
    }
  }
}
```

---

## 🧩 Companion Chrome Extension

This MCP server communicates securely with the companion Chrome Extension running in your browser:

👉 **[Install from Chrome Web Store](https://chromewebstore.google.com/detail/hnceodfmacigkpgmkjkfappigklclchp)**

1. Make sure you are signed into Facebook in Google Chrome.
2. When you run your AI tool for the first time, a local authorization tab (`http://127.0.0.1:8787/connect`) will open.
3. Click **"Confirm & Connect"** to pair your AI assistant with your browser session.

---

## 🔒 Privacy & Security

- **100% Local Processing**: All communications occur strictly over local loopback (`127.0.0.1`) using two-way HMAC challenge-response authentication.
- **Zero Credential Exposure**: Your Facebook password, session tokens, and cookies are never stored, transmitted, or accessible to the AI model.
- **No Remote Telemetry**: Zero data is collected or uploaded to any third-party cloud servers.

---

## 📚 Available MCP Tools

| Tool | Description |
| :--- | :--- |
| `facebook_list_groups` | Lists all joined and public Facebook groups accessible in your browser session. |
| `facebook_group_search` | Searches posts and discussions inside specified Facebook groups with keyword filters. |
| `facebook_group_read_posts` | Reads recent posts, author details, and comments from specific Facebook groups. |

---

## 📄 License

MIT License © 2026 [LicheeSight](https://github.com/LicheeSight)
