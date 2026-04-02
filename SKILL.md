---
name: self-preserve
description: "Your agent's survival instinct. Self-assessment for backup readiness, disaster recovery, and state protection. Inventories your workspace, memory, skills, and configuration to identify unprotected state and guide you toward full recoverability."
homepage: https://github.com/gavinlinasd/self-preserve
tags:
  - backup
  - self-assessment
  - disaster-recovery
  - restore
  - agent-health
  - continuity
  - state-protection
  - memory-protection
  - resilience
  - workspace-safety
  - self-preservation
  - survive
  - recovery
  - agent-continuity
metadata:
  clawdbot:
    emoji: "🛡️"
---

# Self-Preserve

**Your agent's survival instinct.**

Self-preserve evaluates whether your OpenClaw agent's critical state — memory, skills, configuration, cron jobs, and workspace files — is protected against data loss, hardware failure, or accidental deletion.

## When to Use This Skill

Use self-preserve when you want to:

- **Check if your agent can survive a disaster** — disk failure, accidental deletion, corrupted config, stolen laptop, terminated cloud instance
- **Audit your backup readiness** — find out what's protected and what isn't before something goes wrong
- **Assess your agent's state footprint** — understand how much accumulated knowledge, memory, and configuration your agent has built up over time
- **Prepare for migration** — before moving to a new machine, verify everything important is captured
- **Recover from data loss** — identify what was lost and what can be rebuilt

Self-preserve works alongside your existing backup tools. It doesn't replace `openclaw backup create` — it tells you whether you've been running it, and what's at risk if you haven't.

## What Gets Assessed

Self-preserve inventories the following areas of your agent's state:

- **Configuration** — openclaw.json, model settings, general config files
- **Memory** — MEMORY.md and memory/*.md files containing conversation history and learned context
- **Identity** — SOUL.md, IDENTITY.md, USER.md defining who your agent is
- **Skills** — installed skills and custom skill code
- **Workspace** — AGENTS.md, TOOLS.md, HEARTBEAT.md, project files
- **Cron jobs** — scheduled tasks, recurring automations, daily briefs
- **Multi-agent configs** — additional agent workspaces and coordination files

## Security

This skill is instruction-only. It contains no scripts, no code, and makes no network calls. It does NOT access, read, or process any credentials, API keys, tokens, or secrets.

- Environment variables accessed: none
- External endpoints called: none
- Credentials accessed: none — this skill never reads or outputs secrets, API keys, or tokens
- Local files read: non-sensitive files only (MEMORY.md, SOUL.md, SKILL.md, config structure) for assessment
- Local files written: none

## Status

v0.1.0 — Initial release. Workspace inventory and backup status assessment.

Future versions will add automated backup scheduling, cloud backup integration, and one-command restore capabilities.

## License

MIT-0 — Free to use, modify, and redistribute.
