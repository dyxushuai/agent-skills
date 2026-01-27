# AGENTS.md Brainstorming Guide

Use this when requirements are fuzzy and you need a divergent Q&A to discover gaps.

## Rules

- Ask one question per message.
- Prefer multiple choice when possible.
- Keep each question short and concrete.
- Propose 2-3 layout options before drafting.
- Put commands early and require a real code example.

## Decision heuristics

- Single small repo: one root `AGENTS.md` is usually enough.
- Monorepo: keep one `AGENTS.md` with per-app or per-team sections.
- Multiple roles: keep one `AGENTS.md` with role-specific subsections.
- If multiple agents are in scope, confirm expectations but keep a single AGENTS.md unless asked otherwise.
- If Claude Code is in scope, add a CLAUDE.md symlink to AGENTS.md.
- If GitHub Copilot coding agent is in scope, add `.github/copilot-instructions.md` (ideally pointing to AGENTS.md as the source of truth).
- If the repo already has a convention, follow it.

## Divergent option sets (pick 2-3 to propose)

- Structure options (divergent; confirm before writing files):
  1. Root AGENTS.md only (minimal, single-agent friendly).
  2. Root AGENTS.md + CLAUDE.md symlink (Claude Code).
  3. Root AGENTS.md + `.github/copilot-instructions.md` (GitHub Copilot coding agent).
  4. Root AGENTS.md + CLAUDE.md symlink + `.github/copilot-instructions.md` (multi-agent).
  5. Root AGENTS.md + docs/agents/ (long-term documentation; confirm duplication is acceptable).
  6. Other tool-specific files (ask for exact file + path).
- Placement:
  - A) Root `AGENTS.md` (default).
  - B) `docs/AGENTS.md`.
  - C) Other path (ask for exact path).
- Scope boundaries:
  - Path-based (read/write directories).
  - Task-based (docs/tests/lint only).
  - Data-based (no secrets, no prod configs).

## Question bank (ask one at a time)

### Repo shape
- Is this a single app, a monorepo, or a multi-service repo?
- Which languages and frameworks are in active use?
- Are there multiple teams or owners for different paths?

### Placement question
- Where should AGENTS.md live? (A/B/C)

### Agent roles
- Do you want one general scope or multiple role sections inside AGENTS.md?
- Which roles matter most? (docs, tests, lint, API, security, deploy)
- Should any role be read-only?
- Which agents or platforms will consume this AGENTS.md?
- Is Claude Code in scope? If yes, create CLAUDE.md as a symlink to AGENTS.md.

### Tech stack
- What is the exact tech stack with versions and key dependencies?

### Commands
- What are the exact build/test/lint/format commands?
- Are there optional flags or environment requirements?

### Paths and ownership
- Which directories are safe to write to?
- Which paths are read-only or off-limits?

### Standards
- Are there existing code style examples or conventions?
- Any required templates or file formats?
- Can you provide one real code snippet that represents the preferred style?

### Change management
- Branching and commit conventions?
- Any required reviews or CI gates?

### Boundaries and approvals
- What must always be done?
- What requires explicit approval?
- What is never allowed?

## Converge prompt

After 2-4 questions, propose a draft structure and ask for confirmation:

"Based on your answers, I recommend [layout]. Want me to draft the AGENTS.md with that layout?"
