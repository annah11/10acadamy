MCP Setup — Report

MCP-LOG: created rules file and documentation for Tenx MCP setup

What I did

- Created a Tenx-compatible agent rules file at `.github/copilot-instructions.md` (VS Code path).
- Documented the work and next steps in this repository (`REPORT.md` and `README.md`).
- Tuned the rules to follow community best practices (clarity-first, small/testable edits, commit format, safety, and explicit MCP logging).

What worked

- The rules file captures clear constraints and operational guardrails: clarify-before-changing, small commits, testing, non-destructive behavior, and a short MCP log prefix on each agent action.
- Rules align with Boris Cherny / Claude Code community practices: explicit instructions, persona, temperature guidance (low), and fail-safes for large changes.

What didn't work / Limitations

- I could not activate or verify a live connection to the Tenx MCP server from this environment because no TENX_MCP_ID/TENX_MCP_TOKEN credentials or server endpoint were provided.
- I did not install or configure any IDE-specific MCP extensions because that requires network access and user credentials.

Steps I attempted for connection/troubleshooting

- Prepared rules file with an `MCP-LOG:` prefix to ensure Tenx logging captures concise actions when the MCP connection is active.
- Prepared instructions (below) so you can quickly enable the MCP connection in your IDE and validate logging.

How you can enable and verify Tenx MCP connection (VS Code)

1. Install the Tenx MCP / MCP-related extension in VS Code if provided by Tenx.
2. Set environment variables in your shell session (zsh): TENX_MCP_ID and TENX_MCP_TOKEN with the credentials Tenx supplied.
3. Open this workspace in VS Code and ensure the extension picks up the env vars (you may need to restart the editor).
4. Run a sample agent action that the extension logs; confirm Tenx receives entries that include the `MCP-LOG:` prefix.

Files added or changed

- `/.github/copilot-instructions.md` (new) — agent rules and logging
- `/REPORT.md` (new) — this report
- `/README.md` (new) — summary and next steps

Notes and insights

- Rules shape behavior by constraining autonomy: they make the agent explicit (ask clarifying questions), conservative (small, testable changes), auditable (MCP-LOG prefix), and safe (no secrets or destructive actions without approval).
- Good rules improve predictability and traceability, and reduce the risk of unintended large refactors.

If you want, I can:

- Add an example `.vscode/settings.json` to wire environment variables into the workspace.
- Create the same rules file for Cursor (`.cursor/rules/agent.mdc`) or Claude Code (`CLAUDE.md`).
- Attempt to connect and log an MCP action if you provide TENX_MCP_ID and TENX_MCP_TOKEN (do NOT paste secrets here; add them as environment variables in your IDE instead).
