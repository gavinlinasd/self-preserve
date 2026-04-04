# self-preserve

Backup readiness assessment and automated backup scheduling for your OpenClaw agent.

## Install

```bash
npx clawhub@latest install self-preserve
```

## What it does

Self-preserve checks whether your OpenClaw agent's standard state files (config, memory, identity, skills, workspace, cron) are covered by a recent backup. It runs `ls` to check file names and dates, then generates a readiness report showing what's protected and what's at risk.

**New in v0.3.0:** After the assessment, self-preserve can schedule automated backup cron jobs using CronCreate (persistent or session-only). It can also view, update, or remove existing backup schedules using CronList and CronDelete.

It does not read file contents or access credentials. See [SKILL.md](./SKILL.md) for the full assessment steps, safety rules, and scheduling options.

## License

MIT-0
