# Sync Guide

This repository is intended to keep Codex-related working data consistent across multiple computers.

## Daily Workflow

Before starting work on a computer:

```powershell
git pull
```

After finishing work:

```powershell
git add .
git commit -m "Update shared Codex data"
git push
```

## Storage Categories

Use `permanent/` for long-term materials.

Use `codex-cloud/projects/<project-name>/` for Codex cloud-related content grouped by project.

## Safety Rules

Do not commit:

- Passwords
- API keys
- Tokens
- Private certificates
- Local cache files
- Large generated dependency folders

If a save location is unclear, Codex should ask whether the content belongs in `permanent/` or in a project under `codex-cloud/projects/`.

