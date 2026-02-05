## How to use this repo

This repo is a **menu**: pick what you need, adapt it to your project, and contribute improvements back.

### Common ways to use it
- **Reference mode**: open a doc and follow the steps during real work (review, refactor, debugging).
- **Copy mode**: copy a prompt/rule/snippet into your project and tweak it.
- **Standardize mode**: align a team on a shared skill or rule set.

### Where to look
- `rules/`
  - Durable guidance for agents and humans.
  - Organized by language (and later frameworks).
  - Example: `rules/languages/python/use-uv.mdc`.
- `_shared_skills/`
  - Catalog of org-wide Cursor Skills with a standard structure.
  - Use when you want a repeatable workflow (not a one-off answer).

### Rule vs prompt vs skill (when to choose which)
- Use a **rule** when you want consistent behavior across many sessions/files.
- Use a **prompt** when you want a reusable “starter instruction” for a single task.
- Use a **skill** when the task is multi-step and benefits from deterministic checklists and acceptance criteria.

### How to adopt rules in a project
- Copy relevant rule markdown into your project’s Cursor rule setup (team/project rules).
- Keep rules:
  - **Actionable** (commands, checks, do/don’t)
  - **Specific** (versions, tools, constraints)
  - **Short** (prefer links to deeper docs)

### How to use skills
- Treat a skill like a “runbook for an agent”.
- Skills should use **RORO**:
  - Clearly state required inputs (paths, constraints, desired output shape)
  - Clearly state outputs and acceptance criteria

If you’re writing a new skill, follow `_shared_skills/README.md`.

### Contribution workflow (PRs)
When you contribute, aim for small and composable changes:
- Add one rule, prompt, or skill per PR when possible
- Include examples
- State assumptions (OS, language version, toolchain)

### Quality bar (quick)
- Security/privacy: sanitized, no secrets, no client identifiers
- Clarity: someone else can run it without you present
- Repeatability: steps and acceptance criteria are explicit

### Suggested doc style
- Start with intent (“Always…”, “Prefer…”, “Do not…”)
- Provide a short rationale only if it prevents common misuse
- Include copy-pastable commands/snippets
- Keep “happy path” first; add edge cases last

