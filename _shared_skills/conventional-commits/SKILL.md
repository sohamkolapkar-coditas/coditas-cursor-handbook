---
name: conventional-commits
description: Draft conventional commit messages from short change summaries following the Conventional Commits specification. Use when the user asks for commit messages, needs help formatting commits, or when reviewing staged changes for commit.
---

# Conventional Commits

Draft commit messages following the [Conventional Commits](https://www.conventionalcommits.org/) specification.

## Format

```
<type>(<scope>): <subject>

<body>

<footer>
```

**Required**: `<type>: <subject>` (first line)
**Optional**: `<body>` and `<footer>`

## Commit Types

| Type | Use When |
|------|----------|
| `feat` | Adding a new feature |
| `fix` | Fixing a bug |
| `docs` | Documentation changes only |
| `style` | Code style changes (formatting, whitespace) |
| `refactor` | Code refactoring without changing behavior |
| `perf` | Performance improvements |
| `test` | Adding or updating tests |
| `build` | Build system or dependency changes |
| `ci` | CI/CD configuration changes |
| `chore` | Other changes (maintenance, tooling) |
| `revert` | Reverting a previous commit |

## Subject Line Rules

- Use imperative mood: "add feature" not "added feature" or "adds feature"
- No period at the end
- Lowercase (except for proper nouns)
- Max 72 characters
- Be specific and descriptive

## Scope (Optional)

Scope indicates what part of the codebase changed:
- `auth`, `api`, `ui`, `db`, `config`, etc.
- Use lowercase, short noun
- Omit if change spans multiple areas

## Body (Optional)

- Explain **what** and **why**, not **how**
- Wrap at 72 characters
- Use blank line after subject
- Can include multiple paragraphs

## Footer (Optional)

- Reference issues: `Fixes #123`, `Closes #456`
- Breaking changes: `BREAKING CHANGE: <description>`

## Examples

**Example 1: Simple feature**
```
Input: Added user authentication with JWT tokens
Output:
feat(auth): implement JWT-based authentication

Add login endpoint and token validation middleware
```

**Example 2: Bug fix**
```
Input: Fixed bug where dates displayed incorrectly in reports
Output:
fix(reports): correct date formatting in timezone conversion

Use UTC timestamps consistently across report generation
```

**Example 3: Documentation**
```
Input: Updated README with installation instructions
Output:
docs: add installation instructions to README
```

**Example 4: Refactoring**
```
Input: Refactored database connection handling
Output:
refactor(db): simplify connection pool management

Extract connection logic into dedicated module for better testability
```

**Example 5: Multiple changes**
```
Input: Added new API endpoint and fixed bug in error handling
Output:
feat(api): add user profile endpoint

fix(api): handle null values in error responses
```

**Example 6: Breaking change**
```
Input: Changed API response format, breaking existing clients
Output:
feat(api): restructure response payload format

BREAKING CHANGE: Response now wraps data in 'result' object instead of returning directly
```

## Workflow

1. **Analyze the summary**: Identify the primary change type
2. **Determine scope**: What part of codebase changed? (optional)
3. **Write subject**: Imperative mood, specific, under 72 chars
4. **Add body if needed**: Explain context, reasoning, or impact
5. **Add footer if needed**: Reference issues or note breaking changes

## Multiple Changes

If the summary describes multiple unrelated changes, suggest separate commits:

```
Input: Added logging and fixed typo in docs
Output:
chore: add request logging middleware

docs: fix typo in authentication section
```

## Inferring from Context

- Review git diff if available to understand actual changes
- Match commit type to the nature of changes, not just keywords
- Prefer specific scopes over generic ones
- When in doubt between `feat` and `fix`, choose `fix` if it resolves incorrect behavior
