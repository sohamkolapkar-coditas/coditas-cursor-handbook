## Onboarding

This handbook exists to help Coditas teams use Cursor consistently and safely across projects.

If you’re new to Cursor (or new to how we use it), start here.

### What you’ll get from this repo
- **Reusable workflows** you can copy into your project: rules, prompts, and skills
- **Guardrails** for security/privacy, quality, and review
- **Shared vocabulary** so humans and agents mean the same thing

### Redaction is non-negotiable
Before you paste anything into this repo (or into AI chat), verify it contains **no sensitive information**.

Do not include:
- Client names, proprietary project names, repo URLs, ticket links
- Secrets of any kind (tokens, keys, cookies)
- Internal endpoints, IPs, hostnames
- Proprietary source code (keep examples pseudocode-level)

Prefer:
- Generalized patterns, pseudocode, “toy” examples, anonymized snippets
- Before/after descriptions (what changed and why)

(See the root `README.md` for the full policy.)

### A practical first hour
- **Skim the root `README.md`** to understand what contributions we want.
- **Browse `rules/`** for enforceable guidance you can adopt per language/framework.
  - Example: `rules/languages/python/use-uv.mdc`.
- **Browse `_shared_skills/`** to see repeatable agent workflows.
- **Pick one workflow to adopt this week**:
  - A rule set you’ll apply to a project
  - A prompt you’ll reuse
  - A skill you’ll standardize for your team

### How to contribute (the minimum bar)
When you open a PR, include:
- What problem this solves
- Where to place it (rule vs prompt vs skill)
- A short “before vs after” behavior description
- Any assumptions (tools, versions, constraints)

Notes:
- **All files require review** per `CODEOWNERS`.
- If you’re not sure where something belongs, start with a small PR and we’ll reshape it.

### What belongs where (quick decision guide)
- **Rule**: durable guidance the agent should follow in a repo or file pattern (standards, constraints).
- **Prompt**: a reusable instruction template a human copies into Cursor.
- **Skill**: a repeatable multi-step workflow the agent can run with predictable inputs/outputs.

### Checklist for new joiners
- [ ] Read the redaction policy
- [ ] Learn how your team wants to use Cursor (chat vs agent workflows)
- [ ] Adopt at least one rule and one prompt
- [ ] Share one improvement via PR (even small: wording, examples, links)

