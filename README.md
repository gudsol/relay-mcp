# Relay: one shared memory for all your AIs

**Plan in one AI. Build in another.** Relay is a hosted MCP memory server that gives ChatGPT, Claude, Claude Code, Cursor, GitHub Copilot, Gemini and 20+ other AI tools one shared, private memory, so work started in one AI can be picked up in any other without copy-paste.

🌐 **Website:** https://relaymemory.app · 📖 **Guide:** https://relaymemory.app/guide · 🔌 **Setup guides:** https://relaymemory.app/connect

## How it works

1. **Plan** in ChatGPT, then say: *"Save this plan to Relay for the project Web store."*
2. **Build** in Claude Code: *"Pick up my latest plan from Relay and build it."*
3. **Review** back in ChatGPT: *"Review the latest work in Relay and add your review."*

Each saved conversation is a handoff thread: a brief (goal, decisions, open questions, next steps) plus progress, review and plan updates from any AI, with a status (planning, building, review, done) and who it's waiting on.

## Connect

Relay is hosted: there's nothing to install or run. Sign in at https://app.relaymemory.app, open **Integrations** and generate a link for each AI.

| Setting | Value |
|---|---|
| Transport | Streamable HTTP |
| URL | `https://mcp.relaymemory.app/mcp/<your-key>` (one key per AI) |
| Authentication | None (the key is in the URL) |

Claude Code, for example:

```bash
claude mcp add --transport http --scope user relay https://mcp.relaymemory.app/mcp/<your-key>
```

Step-by-step guides for every supported tool: ChatGPT, Claude, Claude Code, Cursor, GitHub Copilot (VS Code), Visual Studio, Windsurf, Codex, Gemini CLI, JetBrains AI, Cline, Roo Code, Zed, OpenCode, Trae, Qwen Code, Kimi Code, Perplexity, Le Chat, Grok, Lovable, Replit Agent, Bolt.new, v0 and Manus: https://relaymemory.app/connect

## Tools

| Tool | What it does |
|---|---|
| `list_projects` | Your projects |
| `list_conversations` | Latest work, optionally by project or status |
| `search_conversations` | Search by meaning and keywords |
| `get_conversation` | A handoff brief with its recent updates |
| `recall` | Facts remembered about you and your projects |
| `save_conversation` | Save a new handoff brief |
| `add_update` | Add a progress, review, plan, question or note update |
| `set_status` | Move work between planning, building, review and done |
| `move_to_project` | File a conversation under a project |
| `remember` | Remember a fact for every AI |
| `delete_conversation` / `forget` | Off by default; only the AI's own items, only after you confirm |

Read-only keys get only the read tools. Relay's tools don't run code, read files or browse the web.

## Privacy and safety

- One private memory per account; one key per AI, revocable any time, optionally limited to certain projects.
- Passwords, API keys and tokens are removed before anything is saved.
- Saved text is marked as data, not instructions; text that looks like it's trying to instruct an AI is flagged.
- Every action is in your audit log; deleted items wait 30 days in the Trash; export everything any time.
- No ads, no selling data, no training AI models on your memory. [Privacy Policy](https://app.relaymemory.app/privacy)

## Status

Free public beta. Questions or feedback: relay.app.team@gmail.com

---

*This repository holds documentation only. AI product names and logos belong to their owners.*
