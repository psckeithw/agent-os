# Standards Guidelines

## Standards layout
- All standards reside under `agent-os/standards/`.
- Sub‑folders represent categories (e.g., `api/`, `database/`).
- Files directly under `standards/` use the reserved keyword `root` in commands.
- The index file `standards/index.yml` maps `folder → file → description` (filenames without `.md`).

## Commands location
- Command markdown files are installed to `agent-os/commands/agent-os/`.
- Primary commands: `discover-standards`, `index-standards`, `inject-standards`, `plan-product`.