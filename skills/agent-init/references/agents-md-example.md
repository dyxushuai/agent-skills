# Complete AGENTS.md Example

This example follows the "commands first" guidance, includes a real code snippet, explicit tech stack with versions, and clear boundaries.

````markdown
# AGENTS.md

## Purpose and scope
You help maintain this repo by making small, safe, well-scoped changes. You must follow the rules below and only touch the approved paths.

## Commands (copy/paste, include flags)
- Build: `pnpm build`
- Test: `pnpm test -- --runInBand`
- Lint: `pnpm lint -- --fix`
- Format: `pnpm format -- --check`

## Tech stack (with versions)
- Runtime: Node 20
- Package manager: pnpm 9
- Framework: Next.js 14, React 18
- Key deps: TanStack Query 5, Zod 3

## Repo map
- `app/` - Next.js app router
- `src/` - shared modules
- `tests/` - unit and integration tests
- `docs/` - documentation
- `scripts/` - tooling

## Code style example (real snippet)
```ts
// Good: explicit errors, clear names
export async function getUserProfile(id: string): Promise<UserProfile> {
  if (!id) throw new Error("User ID required");
  const response = await api.get(`/users/${id}`);
  return response.data;
}
```

## Standards
- Naming: camelCase for functions, PascalCase for types
- Keep changes small and focused
- Update or add tests when behavior changes

## Change management
- Branch names: `feat/<topic>` or `fix/<topic>`
- Commits: Conventional Commits
- PRs: include summary + test results

## Dependencies and environment
- Use `pnpm install`
- Required env vars: `API_BASE_URL`
- Do not add new dependencies without approval

## Boundaries (Always / Ask first / Never)
- Always: run tests for changed areas, update docs if behavior changes
- Ask first: schema changes, dependency additions, CI config changes
- Never: commit secrets, edit `node_modules/`, disable tests
````

If Claude Code is in scope, create a CLAUDE.md symlink to AGENTS.md:

```bash
ln -s AGENTS.md CLAUDE.md
```

If symlinks are not supported in the environment, ask before copying.

If GitHub Copilot coding agent is in scope, add `.github/copilot-instructions.md` and keep it minimal (ideally pointing to `AGENTS.md` as the source of truth).
