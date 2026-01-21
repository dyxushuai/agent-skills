# Agents.md Template

Use the template below. Keep sections short and command-focused. Replace placeholders with repo-specific details.

## Template: Repo-wide AGENTS.md

```markdown
# AGENTS.md

## Purpose and scope
Define what agents do in this repo and what is out of scope.

## Commands (copy/paste, include flags)
- Build: `npm run build`
- Test: `npm test`
- Lint: `npm run lint -- --fix`
- Format: `npm run format`

## Tech stack (with versions)
- Language/runtime: Node 20
- Framework: React 18, Vite 5
- Key deps: TanStack Query 5

## Repo map
- `src/` - application code
- `docs/` - documentation
- `tests/` - test suites
- `scripts/` - tooling helpers

## Code style example (real snippet)
```ts
// Good: descriptive names, explicit errors
export async function fetchUserById(id: string): Promise<User> {
  if (!id) throw new Error("User ID required");
  return api.get(`/users/${id}`).then(r => r.data);
}
```

## Standards
- Naming conventions and formatting rules
- Required checks before changes land

## Change management
- Branching strategy
- Commit format
- PR expectations

## Dependencies and environment
- Runtime versions
- Package manager
- Required environment variables

## Boundaries (Always / Ask first / Never)
- Always:
- Ask first:
- Never:
```

## Claude Code requirement

If Claude Code is in scope, create a CLAUDE.md symlink to AGENTS.md:

```bash
ln -s AGENTS.md CLAUDE.md
```

If symlinks are not supported in the environment, ask before copying.

## Quick prompt to generate a new AGENTS.md

```text
Create an AGENTS.md for this repository. It should list the exact commands to run (with flags), describe the repo structure, include tech stack versions, and provide clear boundaries (always, ask first, never). Keep it short and actionable.
```
