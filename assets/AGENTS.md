<context-hierarchy>
  <parent src="../AGENTS.md" type="global-rules" />
  <system-instruction>
    AGENT: You are operating in the assets bounded context (@vitoria-rodrigues/profile-assets). If you have not read "../AGENTS.md" in this session, stop now and read it using your file-reading tools before proceeding.
  </system-instruction>
</context-hierarchy>

# Bounded Context: assets (`@vitoria-rodrigues/profile-assets`)

This workspace manages canonical design tokens, CSS themes, React SVG icon components, brand lockups, and SVG statistics card templates consumed by `@vitoria-rodrigues/profile-renderer`.

---

## 1. Directory Layout

- **[README.md](./README.md)**: Package usage guide, export map summary, and development scripts.
- **[package.json](./package.json)**: Workspace manifest (`@vitoria-rodrigues/profile-assets`) exporting subpath entrypoints.
- **[src/tokens/](./src/tokens/)**: Brand color scales, CSS custom properties (`tokens.css`), and theme definitions (`theme.css`).
- **[src/icons/](./src/icons/)**: React SVG icon library (`index.tsx`).
- **[src/org/](./src/org/)**: Organization brand marks and SVG lockups (`logos/index.ts`).
- **[src/renderer/](./src/renderer/)**: SVG card templates (`overview.template.svg`, `languages.template.svg`).
- **[src/assets-manifest.json](./src/assets-manifest.json)**: Asset bucket inventory manifest.

---

## 2. Scoped Guardrails

- MUST maintain strict TypeScript typing across token, icon, and logo exports (`pnpm typecheck` and `pnpm lint`).
- MUST keep all exported subpath entrypoints in [package.json](./package.json) synchronized with `src/` assets used by `@vitoria-rodrigues/profile-renderer`.
- MUST preserve `Vitoria-Rodrigues` (`vitoriarodrigues.dev`) brand identity across all manifests, JSDoc headers, and CSS comments.

---

## 3. Required Skills

- **`monorepo-architect`**: Active when updating exports, catalogs, or TypeScript references.
- **`readme-architect`**: Active when updating [README.md](./README.md).
- **`router-architect`**: Active when updating this context router.
