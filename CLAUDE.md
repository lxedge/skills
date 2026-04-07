# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is a skills repository for Claude Code. Each skill extends Claude Code's capabilities with specialized workflows.

## Repository Structure

```
skills/
├── <skill-name>/
│   └── SKILL.md
```

Each skill lives in its own directory with a single `SKILL.md` file.

## SKILL.md Format

Every skill must follow this structure:

```markdown
---
name: skill-name
description: One-line description used in skill listings and triggers
---

# Skill Title

## Overview
Brief explanation of what the skill does.

## When to Use
- Specific trigger conditions
- Use cases
- When NOT to use

## Core Pattern
Step-by-step workflow the skill implements.

## Quick Reference Template
Code or markdown templates the skill uses.
```

### Frontmatter Requirements

- `name`: kebab-case identifier matching directory name
- `description`: Single line, starts with "Use when..." for clarity in skill selection

### Content Guidelines

- Keep skills focused on a single workflow
- Include concrete examples in templates
- Specify file patterns to ignore (e.g., `*.pb.go`, `Justfile`)
- Use clear section headers: Overview, When to Use, Core Pattern, Quick Reference Template

## Creating New Skills

1. Create directory: `mkdir <skill-name>`
2. Create `<skill-name>/SKILL.md` with required frontmatter
3. Commit with message: `feat: add <skill-name> skill`

## Skill Naming

Use kebab-case for skill names. Examples:
- `diff-to-sop`
- `update-config`
- `claude-api`
