# Getting Started

A 5-minute guide to setting up your team AI directives.

---

## Table of Contents

1. [Clone & Customize](#1-clone--customize)
2. [Install as Extension](#2-install-as-extension)
3. [Create a Skill](#3-create-a-skill)
4. [Resources](#4-resources)

---

## 1. Clone & Customize

```bash
git clone git@github.com:YOUR_ORG/team-ai-directives.git
cd team-ai-directives
```

After cloning, customize:

- `context_modules/constitution.md` — Add your team principles
- `context_modules/personas/` — Define your team roles
- `skills/` — Add your capabilities and register them in `.skills.json`

---

## 2. Install as Extension

Use the spec-kit CLI to install this repo as an extension in your project:

```bash
specify init <project> --team-ai-directives https://github.com/your-org/team-ai-directives.git
```

During `specify init`:

- The bundled `team-ai-directives` extension is installed, providing governance commands (`team.discover`, `team.curate`, `team.evolve`, `team.skills`, `team.verify`, `team.repair`) and their matching skills.
- Domain skills listed in `.skills.json` `default[]` are copied to the agent's skills directory.
- The optional `agent-context` extension injects team-directives awareness into the project's context file.

### Available Skills

After installation, the bundled governance skills are available, plus any domain skills registered in this repository's `.skills.json`.

Run verification by invoking the `team.verify` command.

---

## 3. Create a Skill

```bash
mkdir -p skills/my-skill
```

Create `skills/my-skill/SKILL.md`:

```yaml
---
name: my-skill
description: What it does. Use when user asks to [trigger phrases].
---

# My Skill

## Instructions
[Your instructions here]
```

Register it in `.skills.json` so agents can discover and activate it.

---

## 4. Resources

- [AGENTS.md](AGENTS.md) — How agents use this repo
- [.skills.json](.skills.json) — Skills registry
- [context_modules/constitution.md](context_modules/constitution.md) — Core principles
- [README.md](README.md) — Full documentation including Personas and Skills
