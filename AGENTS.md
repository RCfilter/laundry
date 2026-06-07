# AGENTS.md

Guidance for AI agents working in the **laundry** repository (`RCfilter/laundry`).

## Project status

This repository is a **newly initialized skeleton**. As of the initial setup, it contains only `README.md` with the text `laundry init`. There is no application source code, dependency manifest, build configuration, or service definitions yet.

End-to-end development (lint, test, build, run) is **not possible** until project scaffolding and source files are added.

## Tech stack

| Category | Status |
|---|---|
| Languages | Not chosen / not present |
| Package managers | None configured |
| Frameworks | None configured |
| Services | None configured |

## Available system tools (Cloud VM)

The Cloud Agent VM provides:

- **Git** 2.x — repository clone and version control
- **Node.js** v22.x and **npm** 10.x — ready when a Node project is added
- **Python** 3.12 — ready when a Python project is added

Docker is not installed in the default Cloud VM.

## Standard commands (once code exists)

When dependency files are added, use the conventions defined in those files. Typical patterns:

| Task | Likely command (depends on stack) |
|---|---|
| Install deps | `npm install`, `pnpm install`, `pip install -r requirements.txt`, etc. |
| Dev server | `npm run dev`, `python manage.py runserver`, etc. |
| Lint | `npm run lint`, `ruff check .`, etc. |
| Test | `npm test`, `pytest`, etc. |
| Build | `npm run build`, etc. |

Until manifests exist, none of these apply.

## Git workflow

- Default branch: `main`
- Feature branches: `cursor/<descriptive-name>-e777`
- Remote: `https://github.com/RCfilter/laundry`

## Cursor Cloud specific instructions

### Current state

There are **no services to start**. The update script is a no-op because there are no dependencies to refresh on VM startup.

### When application code is added

1. Add the appropriate dependency manifest (`package.json`, `requirements.txt`, etc.) and document install/run commands in `README.md`.
2. Update the VM **update script** (via `.cursor/environment.json` or Cursor Cloud settings) to run the install command — e.g. `npm install` — but **not** dev-server or migration commands.
3. Add service startup notes here (ports, env vars, required external services).
4. If the project uses Docker, note that Docker must be installed separately in the Cloud VM or use a Dockerfile-based environment config.

### Verification without an app

Until code lands, a valid environment check is:

```bash
git status
cat README.md
node --version
python3 --version
```

All should succeed from `/workspace`.
