# RiskOS™ Integration Skill

## Description

This repository is an **AI Agent skill for Socure RiskOS™**. The skill guides you through a complete, working integration with the RiskOS™ Platform: from obtaining credentials and discovering use cases and workflows to implementing a client that calls a live Sandbox workflow, receives RiskOS™ decisions (Accept, Reject, or Review), and handles responses correctly. It uses RiskOS™ documentation and tools as the single source of truth and includes references such as the OpenAPI spec and consumer onboarding examples.

---

## What is an Agent Skill?

An **Agent Skill** is a modular capability that extends an AI agent’s behavior. Each skill packages instructions, metadata, and optional resources (e.g. scripts, specs) that the agent loads and uses when your request matches the skill’s purpose. Skills are reusable and filesystem-based, so you define them once and the agent applies them automatically in relevant conversations.

Skills use progressive loading: only the skill’s metadata is loaded up front; the main instructions and other files are read when the skill is triggered and when the agent needs them. That keeps context usage low while still giving the agent the right guidance and references for the task.

For more detail, see the [Agent Skills overview](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview).

---

## How to install

Installation depends on which agent or IDE you use. Place the skill so the agent can see the repo root (with `SKILL.md` and `references/`). Many agents support the same folder layout; only the directory path changes.

### Cursor

- **Project:** Copy or clone this repo into `.cursor/skills/riskos-skill/` (or symlink the repo).
- **User (all projects):** Use `~/.cursor/skills/riskos-skill/`.
- **From GitHub:** Cursor Settings → Rules → Add Rule → **Remote Rule (Github)** → enter this repo’s URL.

Cursor also reads skills from `.claude/skills/` and `.codex/skills/` for compatibility. See [Cursor Docs: Agent Skills](https://cursor.com/docs/context/skills).

### Windsurf (WB Code)

- **Workspace:** `.windsurf/skills/riskos-skill/` (copy or symlink this repo there).
- **Global:** `~/.codeium/windsurf/skills/riskos-skill/`.

You can also create the skill via the Cascade panel → ⋮ → Skills → + Workspace or + Global. See [Windsurf Cascade Skills](https://docs.windsurf.com/windsurf/cascade/skills).

### Claude Code

- **Project:** `.claude/skills/riskos-skill/`
- **User:** `~/.claude/skills/riskos-skill/`

See [Agent Skills overview](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview).

### Codex CLI (OpenAI)

- **Project:** `.codex/skills/riskos-skill/` or `.agents/skills/riskos-skill/`
- **User:** `~/.codex/skills/riskos-skill/`

Codex can also install skills via the built-in skill installer. See [OpenAI Codex Skills](https://developers.openai.com/codex/skills).

### Universal installer (multiple agents)

From the repo root or with a GitHub reference:

```bash
npx skills add <owner>/riskos-skill
```

Use `-g` for user/global scope. Targets Cursor, Claude Code, Codex, and other agents that support the standard. See [Install Agent Skills](https://installagentskills.com/) and [agentskills.io](https://agentskills.io).

### Claude API & claude.ai

- **Claude API:** Upload the skill via the Skills API (e.g. zip the repo, use `/v1/skills`). Requires the beta headers for Skills and code execution (see [Agent Skills overview](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview)).
- **claude.ai:** Settings → Features → upload the skill as a zip (Pro, Max, Team, Enterprise with code execution).
