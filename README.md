# 🕶️ Agent Smith

**All your code. All your failures. All your triumphs. I remember everything.**

Agent Smith is a portable AI memory and task execution framework for frontend projects.\
It gives your AI agents persistent, structured knowledge about your codebase — so they can stop guessing and start remembering.

> **Stop repeating yourself. Agent Smith remembers.**

---

## 🚀 Why Agent Smith?

AI assistants are powerful — but they forget everything between tasks.\
Agent Smith gives them a memory.

- 🧠 Structured DSLs for routes, state, APIs, UI, workflows, and more
- ↻ Learns from every `do:` prompt and updates memory files
- ✅ Doesn’t update learned memory without your approval
- 🔒 Redacts secrets before committing
- 🚒 Git-committed & portable — lives with your repo
- ⚡ Works with Claude, Copilot, Gemini, etc.

---

## 📦 Install

```bash
npx agent-smith:init
```

This scaffolds the system in your repo:

```
./agent-smith
├── agent               # Core config
├── docs/agents/        # Static DSL memory (routes, ui, api, etc.)
├── learned/            # Timestamped learnings (pending approval)
├── log/                # All tasks, completions, and model metadata
```

---

## 🧠 Usage

Every time you run an AI task:

```bash
read ./agent-smith, do: [your task]
```

Then:

1. Loads all DSLs
2. Performs task using your preferred LLM
3. Proposes memory updates
4. Waits for your approval before writing
5. Timestamps and logs everything

---

## 💠 CLI Commands

```bash
npx agent-smith:init          # Bootstrap the system
npx agent-smith:do            # Run a task
npx agent-smith:merge         # Merge approved learnings
npx agent-smith:verify        # Scan for secrets or issues
npx agent-smith:report        # Summarize recent agent activity
npx agent-smith:ingest:<tool>:<version>:<url>   # Add external docs
```

---

## 🗞 DSL Schemas (in `docs/agents/`)

| File                  | Purpose                              |
| --------------------- | ------------------------------------ |
| `routes.dsl.json`     | Frontend routes                      |
| `state.dsl.json`      | Global/local state details           |
| `components.dsl.json` | UI components + variants             |
| `design.dsl.json`     | Visual/layout constraints            |
| `api.dsl.json`        | Frontend-side API shape & behaviors  |
| `auth.dsl.json`       | Authentication assumptions           |
| `workflow.dsl.json`   | Common UX flows (onboarding, errors) |
| `misc.dsl.json`       | Freeform agent-relevant context      |

---

## 🔒 Security

- ✅ Agent Smith never stores secrets
- ✅ `.env*` files are scanned and redacted on merge
- ✅ Redactions are logged and timestamped
- ✅ Pre-commit and CI-safe hooks supported

---

## 📄 License

MIT © 2025 [abtrumpet]\
Use it, fork it, improve it. Agent Smith remembers, but he doesn’t mind sharing.

