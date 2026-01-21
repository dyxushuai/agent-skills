# Agent Init Skills

A small set of skills for initializing and maintaining AGENTS.md files.
Designed to replace ad hoc "init" prompts with a consistent, repo-aware workflow.

Reference (best practices + starter template):
https://github.blog/ai-and-ml/github-copilot/how-to-write-a-great-agents-md-lessons-from-over-2500-repositories/#starter-template

Skills follow the Agent Skills specification: https://agentskills.io

## Available Skills

### agent-init

Create or improve AGENTS.md files that define how coding agents operate in a repo.

Use when:
- Setting up an initial AGENTS.md
- Replacing an agent "init" command with a durable AGENTS.md
- Standardizing multi-agent behavior across a repo
- Auditing an existing AGENTS.md for missing commands or boundaries
- Using Claude Code (requires CLAUDE.md symlink to AGENTS.md)

Location: `skills/agent-init`

## Installation

Install all skills from this repo:

```bash
npx add-skill dyxushuai/agent-skills
```

Install only agent-init:

```bash
npx add-skill dyxushuai/agent-skills --skill agent-init
```

List skills:

```bash
npx add-skill dyxushuai/agent-skills --list
```

## Best Practices Summary

Follow GitHub's guidance: put commands early (with flags), include at least one real code example, specify tech stack versions, and use Always / Ask first / Never boundaries; keep AGENTS.md short, concrete, and repo-specific.

## Usage

Skills are available once installed. The agent will use them when the request matches.

### Codex example

```
$agent-init
Create AGENTS.md with exact build/test/lint commands and boundaries.
```

### Claude example

```
/agent-init
Create AGENTS.md with exact build/test/lint commands and boundaries.
Keep it short and command-first.
Create CLAUDE.md as a symlink to AGENTS.md.
```

### Other prompts

- "Audit our existing AGENTS.md for missing boundaries and commands."
- "Update AGENTS.md to include the current test and lint commands."
- "Add CLAUDE.md as a symlink to AGENTS.md for Claude Code."

## Skill Structure

Each skill contains:
- `SKILL.md` - instructions for the agent
- `references/` - supporting documentation (optional)
- `scripts/` - helper scripts (optional)

## Compatibility

Skills are plain Markdown with YAML frontmatter and work across multiple agents.
Install with add-skill for Codex, Claude, Cursor, and others.
If Claude Code is in scope, create CLAUDE.md as a symlink to AGENTS.md.
