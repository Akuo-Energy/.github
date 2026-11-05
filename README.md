# Akuo-Energy organization defaults

This repository contains shared contribution guidance and pull request defaults for repositories owned by the Akuo-Energy organization.

## Files

- [`CONTRIBUTING.md`](CONTRIBUTING.md) defines organization-wide pull request practices, Squash and merge, branch-name and title conventions, and the GitHub-generated revert title exception.
- [`PULL_REQUEST_TEMPLATE.md`](PULL_REQUEST_TEMPLATE.md) provides a generic PR description template for repositories without their own template.

Keep repository-specific instructions in that repository. For example, a data-platform repository may have Fabric workspace, notebook, dependency, and test guidance in its local `.github/CONTRIBUTING.md`; those requirements do not apply to other Akuo-Energy repositories.

## How GitHub applies these defaults

For these files to be used as organization defaults, this repository must be named exactly `.github` and be public. GitHub uses each repository's own community health file or pull request template in preference to the corresponding default here. A local file replaces the default rather than merging with it, so local guides should link to the organization-wide conventions when both apply.

To adopt the generic PR template in a repository, remove or rename its local PR template. Keep a local template when that repository needs additional review or validation questions.
