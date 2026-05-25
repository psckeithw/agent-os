# Installation Guidelines

## Installation
- Run `scripts/project-install.sh` from your project root.
- Default profile is `default` from `config.yml`; override with `--profile <name>`.
- Use `--commands-only` to install only the command definitions.
- The script aborts if run inside the Agent OS base directory or without a valid profile.

## Profile & inheritance
- Profiles live in `profiles/<name>/` and can inherit via `inherits_from` in `config.yml`.
- The effective inheritance chain is displayed during installation.