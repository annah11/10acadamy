Tenx MCP Setup — Repository

MCP-LOG: created repository docs for Tenx MCP challenge

Overview

This repository contains the agent rules and documentation for the Tenx MCP setup challenge. The primary rules file is `.github/copilot-instructions.md` (for VS Code). If you use Cursor or Claude Code, copy the contents into `.cursor/rules/agent.mdc` or `CLAUDE.md` respectively.

Files added

- `.github/copilot-instructions.md` — Agent rules and logging format
- `REPORT.md` — What I did, what worked, challenges, and next steps
- `README.md` — This overview and quickstart

Quickstart to enable Tenx MCP in VS Code

1. Ensure the Tenx MCP extension is installed in VS Code.
2. Set environment variables in a terminal (zsh):
   - export TENX_MCP_ID="<your-id>"
   - export TENX_MCP_TOKEN="<your-token>"
3. Open VS Code in this workspace and restart the editor.
4. Run an agent action and verify the Tenx dashboard shows entries with `MCP-LOG:` in the message.

Next steps

- If you prefer Cursor or Claude Code, I'll add the corresponding rules file.
- I can prepare a `.vscode` folder with recommended settings and tasks to run tests and formatting automatically.
