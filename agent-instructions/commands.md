# Commands Guidelines

## Discover Standards (`/discover-standards`)
- Interactive workflow: determines focus area, analyzes representative files, asks the user for clarification, drafts standards, confirms creation, updates the index.
- Always uses the `AskUserQuestion` tool for any user prompt.

## Index Standards (`/index-standards`)
- Scans `standards/` for `.md` files, builds/updates `index.yml`.
- Prompts the user for one‑sentence descriptions for new files.
- Deletes stale entries automatically.

## Inject Standards (`/inject-standards`)
- **Auto‑suggest mode** (no args): reads `index.yml`, matches descriptions against current context, presents 2‑5 suggestions, then injects based on detected scenario (conversation, skill, planning).
- **Explicit mode** (`/inject-standards <folder>[/<file>] …`): injects the specified standards directly.
- Scenario detection rules:
  1. Planning – conversation mentions “spec”, “plan”, or “shape”.
  2. Skill creation – mentions `agent-instructions/skills/` or building a reusable skill.
  3. Otherwise **ask** the user to confirm the scenario.
- Use `root` to refer to standards in the top‑level folder.
- Errors list available standards when a name isn’t found.

## Plan Product (`/plan-product`)
- Generates `agent-os/product/mission.md`, `roadmap.md`, `tech-stack.md` via interactive Q&A.
- If a `global/tech-stack.md` standard exists, it is offered as a base.
- Files are created under `agent-os/product/`.