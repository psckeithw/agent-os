# Workflow Guidelines

## General interaction rule
- Never ask the user anything without the `AskUserQuestion` tool.
- Keep prompts singular and lightweight.

## Typical workflow
1. Install Agent OS with `scripts/project-install.sh`.
2. Run `/discover-standards` to capture project patterns.
3. Run `/index-standards` (auto‑run by discover).
4. Use `/inject-standards` at the start of a task to load relevant standards.
5. Optionally run `/plan-product` for high‑level documentation.

## Gotchas
- The `root` keyword cannot be a real directory; it only references files directly under `standards/`.
- Index descriptions must be a single sentence; longer text will be ignored.