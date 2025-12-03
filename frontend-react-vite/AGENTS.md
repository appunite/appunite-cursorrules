# Repository Guidelines

## Project Structure & Module Organization

- `src/` hosts the Vite React app: `main.tsx` boots `App.tsx`, `api/` holds generated clients, `dataDirectory/` owns domain logic, and `ui/` stores shared components.
- Tests sit beside code in `__tests__` folders (e.g., `src/dataDirectory/utils/__tests__/menuLayoutHelpers.test.ts`).
- Assets live in `public/`, bundles land in `dist/`, and tooling config sits in `vite.config.ts`, `eslint.config.js`, `prettier.config.js`, `bunfig.toml`, and `mise.toml`.

## Build, Test & Development Commands

- `bun install` — install dependencies.
- `bun run dev` — start Vite locally; ensure `.env.local` defines `VITE_API_BASE_URL`.
- `bun run lint`, `format:check`, `typecheck` — run before pushing.
- `bun run test` — execute Vitest (watch mode starts by default, not to run it add `--run`, `--coverage` for deep changes).
- `bun run build` — compile and emit `dist/`.

## Coding Style & Naming Conventions

- ESLint + Prettier enforce 2-space indent, single quotes, no semicolons, and 90-character lines; run `bun run lint:fix` or `bun run format` for bulk cleanups.
- Components use PascalCase, hooks/utilities use camelCase, env exports stay SCREAMING_SNAKE_CASE; co-locate helper types with their feature.
- Prefer Tailwind utilities; reach for CSS modules only when utilities fall short.

## Testing Guidelines

- Vitest with Testing Library drives behavior checks; snapshot tests should stay rare and reviewed.
- Name files `<subject>.test.ts` inside the nearest `__tests__` directory.

## Commit & Pull Request Guidelines

- Commits remain short, imperative, and scoped (`add menu pages ui`); split refactors from features.
- PR titles must follow Conventional Commit syntax (`feat(scope): summary`) using one of the allowed scopes (`ui`, `core`, `contrib`, `api`) and must NOT end with a trailing period or ellipsis; squash merges reuse that title for release-please.
- Labels auto-apply from `.github/labeler.yml`; sub-folder labels exist for `src/api`, `src/auth`, `src/dataDirectory`, `src/observability`, and `src/ui`. The pre-commit hook runs `bun run verify:labels` to ensure new subdirectories get coverage.
- Document PR intent, QA steps, linked issues, and UI screenshots or GIFs when relevant.

## CI & Release Automation

- `.github/workflows/ci.yml` runs on PRs and `main`, using Bun to install, verify label coverage, lint, format-check, type-check, test (JUnit + Test Reporter), and build; artifacts are attached for reviewers.
- `.github/workflows/release-please.yml` turns merged `main` commits into versioned releases, then builds the tagged commit, uploads `wombat-dist-<version>.tar.gz`, and publishes a bundle-size delta against the prior release.

## Environment Notes

- Track required variables in `.env.example` and add validations in `src/env.ts`. Keep new keys documented.
- Provision `GH_PAT_TOKEN` (classic PAT with `repo` scope) for release automation and rotate it when team membership changes.
- Keep the `README.md` header and wombat image intact when updating project documentation; downstream materials reference that layout.
