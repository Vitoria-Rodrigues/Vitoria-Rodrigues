# Vitoria-Rodrigues Profile Monorepo Agents Context

This document serves as the sovereign root context router (Layer 1) for AI agents operating in the `Vitoria-Rodrigues/Vitoria-Rodrigues` (`vitoriarodrigues.dev`) monorepo.

## Navigation

- [README.md](./README.md): Dynamic GitHub Profile view (compiled by `@vitoria-rodrigues/profile-renderer` from [renderer/src/pipelines/readme/readme.template.md](./renderer/src/pipelines/readme/readme.template.md)) with workspace architecture inside a collapsible details block.
- [.agents/plugins.json](./.agents/plugins.json): Antigravity plugin registry importing domain plugins from `@vitoria-rodrigues/agent-mesh`.
- [renderer/AGENTS.md](./renderer/AGENTS.md): Dynamic asset generator and document compilation engine (`@vitoria-rodrigues/profile-renderer`).
- [assets/AGENTS.md](./assets/AGENTS.md): Design tokens, brand icons, and SVG card templates (`@vitoria-rodrigues/profile-assets`).

## Architecture

The repository is a Turborepo + pnpm monorepo (`catalogMode: strict`) automating GitHub profile stats generation and governance document compilation:

- **`renderer/` (`@vitoria-rodrigues/profile-renderer`)**: TypeScript pipeline engine compiling `README.md`, `CODE_OF_CONDUCT.md`, `LICENSE.md`, and SVG stats cards from GitHub GraphQL API metrics.
- **`assets/` (`@vitoria-rodrigues/profile-assets`)**: Design tokens, brand logos, React SVG icons, and SVG card templates consumed by the renderer pipeline.
- **`scripts/`**: Root Git hook scripts (`pre-commit.ts`, `prepare-commit-msg.ts`) executed via Husky.

## Scoped Guardrails

- MUST maintain a strict senior, objective, and technical tone across all communications, logs, and documentation.
- MUST conduct conversational chat responses in Brazilian Portuguese (pt-BR) while keeping all code, configuration files, commit messages, `AGENTS.md`, and `README.md` files in English (en-US).
- MUST NOT use emojis in any conversational response, code comment, technical document, README, or commit message (Zero-Emoji Invariant).
- MUST edit `renderer/src/pipelines/readme/readme.template.md` (not only root `README.md`) whenever updating the root profile README so scheduled CI runs preserve changes.
- MUST use `pnpm` exclusively and consume all dependencies via `catalog:` entries in [pnpm-workspace.yaml](./pnpm-workspace.yaml).
- MUST consume `@vitoria-rodrigues/agent-mesh` solely via `catalog:plugins-stack` and `.agents/plugins.json` without duplicating local skills or rules inside `.agents/`.
- MUST format all files according to Prettier standards (2-space indent, max 100-character line width).
- MUST use relative paths for all Markdown links; absolute `file:///` paths are strictly forbidden.
- MUST use Conventional Commits v1.0.0 (`<type>(<scope>): <description>`) and sign commits with SSH (`git commit -S -m "..."`) when `user.signingkey` is configured.

## Required Skills

When operating in this monorepo, agents MUST activate the relevant `@vitoria-rodrigues/agent-mesh` skill:

- **`router-architect`**: Active when creating, updating, or auditing any `AGENTS.md` context router.
- **`readme-architect`**: Active when creating, updating, or auditing any `README.md` documentation or template.
- **`monorepo-architect`**: Active when auditing `pnpm-workspace.yaml` catalogs, `turbo.json`, `tsconfig*.json`, or `package.json` manifests.
- **`github-flow-operator`**: Active when creating branches, commits, pull requests, or maintaining `.github/workflows/`.
