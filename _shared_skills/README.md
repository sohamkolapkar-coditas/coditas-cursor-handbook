## Coditas Shared Skills (Wide Adoption)

This folder is a **catalog of reusable Cursor Skills** that Coditas teams can adopt consistently across projects.

### What belongs here

- **Shared, organization-wide workflows**: standards, release processes, code-review routines, commit conventions, incident workflows
- **Repeatable engineering tasks**: scaffolding, API patterns, testing practices, documentation conventions
- **Tooling integrations**: linters, formatters, CI checks, templates that the agent should follow

### Skill directory structure

Each skill lives in its own folder:

```
_shared_skills/
  <skill-name>/
    SKILL.md
```

Naming convention:
- **Folder name**: lowercase with hyphens (e.g. `conventional-commits`)
- **Skill file**: `SKILL.md`

### Skill entry placeholders (standard sections)

Use these placeholders when creating new skills so they’re consistent and easy to adopt.

- **Frontmatter (required)**
  - `name`: short, unique id (match folder name)
  - `description`: one sentence describing what it does + when to use it

- **Problem statement**
  - What problem does this skill solve?
  - Who should use it (roles/teams)?

- **When to use (triggers)**
  - Example user prompts that should invoke the skill
  - Any “do NOT use when …” constraints

- **Inputs (RORO)**
  - What info the agent needs (e.g., change summary, target file paths, environment constraints)

- **Outputs**
  - What the skill produces (e.g., message template, commands to run, PR description, file changes)

- **Workflow / steps**
  - A short, deterministic checklist the agent can follow

- **Edge cases**
  - Common pitfalls and how to handle them

- **Examples**
  - At least 2–3 input → output examples

- **Acceptance criteria**
  - How to verify the result is “done”

- **References**
  - Links to internal guidelines, RFCs, or external specs

### Skills table

| Sr. No | Skill name | What it does | When it is used |
|---:|---|---|---|
| 1 | `conventional-commits` | Drafts commit messages following the Conventional Commits spec (type/scope/subject/body/footer). | When the user asks for a commit message, wants help formatting commits, or needs guidance choosing `feat`/`fix`/etc. |

### Adding a new skill (checklist)

- Create folder: `_shared_skills/<skill-name>/`
- Add `SKILL.md` with the placeholders above
- Keep the skill **tool-agnostic** unless it requires specific tooling (then document versions/assumptions)
- Update the table in this file with a new row
