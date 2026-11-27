# Assets Package (`@vitoria-rodrigues/profile-assets`)

The `assets` package (`@vitoria-rodrigues/profile-assets`) exports brand identity assets, design system tokens, CSS theme definitions, React SVG icon components, and SVG card templates.

---

## Package Contents

- **[src/tokens/](./src/tokens/)**: CSS variables, color scales, and theme configuration.
- **[src/icons/](./src/icons/)**: React SVG icon library.
- **[src/org/](./src/org/)**: SVG logos and identity mark source files.
- **[src/renderer/](./src/renderer/)**: SVG card templates for stats and language generation.
- **[src/assets-manifest.json](./src/assets-manifest.json)**: Asset inventory manifest.

---

## Usage in Monorepo

Import styles, tokens, and components directly in consuming packages:

```tsx
import { brandColors } from '@vitoria-rodrigues/profile-assets/tokens';
import '@vitoria-rodrigues/profile-assets/theme.css';
```

---

## Development Scripts

| Command          | Description                                                      |
| :--------------- | :--------------------------------------------------------------- |
| `pnpm typecheck` | Validates TypeScript compliance across assets and token exports. |
| `pnpm lint`      | Runs ESLint and Prettier checks.                                 |
