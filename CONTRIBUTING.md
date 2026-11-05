# Contributing to Akuo-Energy repositories

These are the organization-wide conventions for pull requests and branch names. A repository may add its own `CONTRIBUTING.md` for project-specific workflows; that guide should link here and clearly distinguish local requirements from these shared conventions.

## Pull request workflow

- Use **Squash and merge**. The pull request title becomes the commit title on the target branch, so it must follow the title convention below.
- Use the repository's pull request template. Explain the motivation and changes, and describe the relevant validation performed.
- Follow the target repository's contribution and merge strategy: target branch, required reviews, checks, and merge methods can differ between repositories.
- Check for a `CODEOWNERS` file to identify the people or teams responsible for the changed files and request their review where appropriate. `CODEOWNERS` identifies ownership; repository rulesets or branch protection determine whether an owner's approval is required and who can merge.
- Update relevant documentation when behavior or usage changes.
- Do not commit credentials, personal tokens, or generated local environment files.

## Pull request titles

Use this format for pull request titles and the resulting squash commit title:

```text
<type>(<scope>)!: <description>
```

- `type` is required and lowercase.
- `(scope)` is optional. Use lowercase letters, digits, hyphens, underscores, or slashes, for example `ingestion-clients` or `fabric/ot`.
- `!` is optional and marks a breaking change. Place it after the optional scope.
- Use exactly one space after the colon.
- Keep the complete title to 72 characters or fewer.
- Write the description in English, clearly and actionably.

Allowed types:

| Type | Use |
| --- | --- |
| `feat` | New functionality |
| `fix` | Bug fix |
| `docs` | Documentation only |
| `style` | Formatting or style changes without logic changes |
| `refactor` | Code restructuring without a feature or bug fix |
| `perf` | Performance improvement |
| `test` | Adding or changing tests |
| `build` | Packaging and dependencies, such as `pyproject.toml` or `uv.lock` |
| `ci` | CI workflows and automation |
| `chore` | Maintenance that does not change application code or tests |

Examples:

```text
feat: add Bazefield allocations endpoint
fix(ingestion-clients): retry requests on 429
feat(fabric/ot)!: rename gold tables
ci(tests): add required check
```

Avoid vague descriptions such as `update`, `changes`, or `fix bug`.

### Reverts

There is no `revert` type. When reverting a merged pull request, use GitHub's **Revert** button and keep its generated title:

```text
Revert "<original title>"
```

This generated format is accepted as an exception to the standard title format and length limit.

## Branch names

Use this format for feature branches:

```text
<type>/<description>
```

- Use one of the types listed above.
- Use lowercase letters and digits in the description, with hyphens between words.
- A Jira ticket key may optionally prefix the description.
- Keep the scope in the description rather than adding another `/` separator.

Examples:

```text
feat/data-520-bazefield-allocations
fix/fabric-ot-default-lakehouse
ci/tests-required-check
```

The following are exceptions: `main`, GitHub-generated revert branches (`revert-<number>-...`), and `dependabot/...` branches.

## Repository-specific guidance

Follow any additional contribution requirements documented in the target repository. Those local requirements apply only to that repository and do not change these organization-wide conventions.
