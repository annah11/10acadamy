# Tenx MCP Setup Repository

Concise documentation and agent rules for the Tenx MCP setup challenge.

## Overview

This repository provides the rules and documentation needed to validate Tenx MCP logging in your IDE. The primary rules file is located at .github/copilot-instructions.md for VS Code. If you use Cursor or Claude Code, copy the contents to .cursor/rules/agent.mdc or CLAUDE.md respectively.

## Repository Contents

- .github/copilot-instructions.md — Agent rules and logging format
- REPORT.md — What was done, what worked, challenges, and next steps
- README.md — This overview and quickstart

## Quickstart (VS Code)

1. Install the Tenx MCP extension in VS Code.
2. Set environment variables in your shell:
   - export TENX_MCP_ID="<your-id>"
   - export TENX_MCP_TOKEN="<your-token>"
3. Open this workspace in VS Code and restart the editor.
4. Run an agent action and confirm the Tenx dashboard shows entries containing MCP-LOG:.

## Next Steps

- Add the Cursor or Claude Code rules file if needed.
- Add a .vscode configuration for repeatable tasks and formatting.
