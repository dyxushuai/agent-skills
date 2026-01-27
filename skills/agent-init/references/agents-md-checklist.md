# AGENTS.md Review Checklist

Use this checklist to audit an existing AGENTS.md file.

## Command-first checks

- [ ] Commands section appears near the top (before repo map or standards).
- [ ] Commands include flags/options, not just tool names.
- [ ] Commands are copy/paste ready (no placeholders).

## Essentials

- [ ] Clear role or persona (not a generic helper).
- [ ] Specific scope and non-goals are stated.
- [ ] Commands appear early and include flags/options.
- [ ] Tech stack and versions are explicit.
- [ ] Key directories and ownership are listed.

## Six core areas

- [ ] Purpose and scope
- [ ] Repo map and code organization
- [ ] Run/test/validate commands
- [ ] Change management
- [ ] Dependencies and environment
- [ ] Boundaries and avoid list

## Boundaries and safety

- [ ] Always / Ask first / Never sections are present.
- [ ] Sensitive areas are protected (secrets, vendor, prod config).
- [ ] Dependency changes or schema changes require approval.

## Examples and standards

- [ ] At least one real code snippet or output example.
- [ ] Style guidance is concrete, not abstract.

## Clarity and brevity

- [ ] Every rule maps to a command, path, or policy.
- [ ] No vague directives like "run tests" without commands.
- [ ] File is short enough to scan quickly.

## Multi-agent readiness

- [ ] Guidance works across agents (plain Markdown, no tool-specific fields unless required).
- [ ] Role scoping is clear inside AGENTS.md (sections or labels).
- [ ] If Claude Code is in scope, CLAUDE.md is a symlink to AGENTS.md.
