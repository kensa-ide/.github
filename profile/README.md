<p align="center">
  <a href="https://kensa-ide.com">
    <img src="https://kensa-ide.com/brand/kensa-wordmark.svg" alt="Kensa" width="240">
  </a>
</p>

<h1 align="center">QA test-management in your repo</h1>

<p align="center">
  Test cases as plain Markdown under git, edited by your own terminal AI agent.<br>
  No server. No cloud. No bundled AI.
</p>

<p align="center">
  <a href="https://kensa-ide.com/download">Download</a> ·
  <a href="https://kensa-ide.com/docs/getting-started">Getting started</a> ·
  <a href="https://kensa-ide.com/docs/cli">CLI reference</a> ·
  <a href="https://kensa-ide.com/plugin">Kensa-QA plugin</a> ·
  <a href="https://kensa-ide.com/feedback">Feedback</a>
</p>

---

## What is Kensa

Kensa is a desktop IDE for QA engineers. Write, review, and maintain test cases like code: every case is a Markdown file in your own git repository. Import cases from an existing TMS and work locally, or run Kensa as your full-cycle test-management system. Your data never lives on someone else's server.

Available for **Windows** and **macOS**.

## The pieces

### 🖥 Kensa IDE

The editor plus the utilities QA reaches for every day, without leaving the app:

- **Browser** — launch and drive Chrome over CDP, wire routines to the CLI so an agent can open a page, check it, and write the result back to the case
- **HTTP runner** — file-first REST client
- **Mobile commands** — iOS & Android presets
- **Regex tester, JWT decoder, JSON diff, timestamp converter**

### ⚙️ Kensa CLI

A 30-command binary ships with the app, already on your terminal's PATH. Built for both humans and AI agents: navigate large test bases, filter, lint, dedupe, check coverage and traceability. Migration runs both ways — import cases in, export them back to your TMS.

```bash
~/acme-tests ❯ kensa filter "tag:smoke and priority:high" --format ids
AUTH-218 AUTH-219 CART-104 CART-110

~/acme-tests ❯ kensa lint
✓ 312 cases · 0 errors · 3 warnings
```

### 🤖 Kensa-QA plugin — [`QA_agents`](https://github.com/rpluzhnikov/QA_agents)

A manual-QA team inside Claude Code or OpenAI Codex. Point it at a ticket — Linear, Jira, Confluence, Notion, Figma, or free text — and get committed test cases back. **Free, MIT, no API keys.**

How it works: a Test Lead reads project memory, pulls the spec via MCP, and builds a plan. You approve it. QA Engineers spawn in parallel — checklist, review, cases — and the Lead reviews everything before it lands in `.tms/suites/`. Every agent draws on a library of 31 skills grounded in ISTQB.

| Command | What it does |
|---|---|
| `/setup` | Bootstraps `.tms/memory/` and `.mcp.json`, learns your style from existing cases |
| `/new-feature <ref>` | Pulls spec, plans, you approve, engineers write cases |
| `/update-feature <ref>` | Finds cases by `source_id`, rewrites only what changed |
| `/brainstorm <topic>` | Three strategists deliberate contested scope; you pick the winner |
| `/audit` | Schema validation, duplicates, drift, tag check across `.tms/` |
| `/risk-assess`, `/test-plan`, `/traceability`, … | Analysis commands — read-only, one committable artifact each |

Install for Claude Code:

```bash
/plugin marketplace add rpluzhnikov/QA_agents
/plugin install kensa-qa@rpluzhnikov
```

### 🧩 Blueprints

Node-graph automation on a canvas: call APIs, run shell checks, loop and branch, and drive Claude Code or Codex as a first-class step. Every blueprint is a plain JSON file in your repo. [Explore Blueprints →](https://kensa-ide.com/blueprints)

## Principles

- **Local-first.** Cases, memory, blueprints — all plain files under git.
- **Bring your own agent.** Kensa doesn't bundle an AI; it gives your terminal agent a CLI and a plugin to work with.
- **Design, don't execute.** The agent suite reasons about tests and writes them; it does not run them.
- **Human gates.** Plans and strategy decisions always pass through you before anything is written.

## It's just me on the other end

Kensa is a one-person project — I write the code, fix the bugs, and read the email. Whatever you send lands on my desk, and bugs usually ship fixed within days.

- 🐛 [Report a bug / send an idea](https://kensa-ide.com/feedback)
- 💬 [GitHub Issues](https://github.com/rpluzhnikov/QA_agents/issues)
- 👤 [@rpluzhnikov](https://github.com/rpluzhnikov) · [LinkedIn](https://www.linkedin.com/in/pluzhnikov-roman)

---

<p align="center">検 © 2026 Kensa</p>
