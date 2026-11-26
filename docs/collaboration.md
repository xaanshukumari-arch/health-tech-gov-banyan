# Pull Request Collaboration

## Team workflow

1. Track each change in a GitHub Issue and create a focused feature branch from `develop`, following the [branching strategy](./branching-strategy.md).
2. Push the branch and open a pull request targeting `develop`.
3. Link the issue in the pull request. Use `Closes #<number>` only when merging the pull request fully completes the issue; otherwise use `Refs #<number>`.
4. Ask a project maintainer to assign an appropriate reviewer. The author should respond to feedback and update the branch before merge.
5. Merge only after required approvals and automated checks pass. Delete the feature branch after merge.

## GitHub setup still required

Repository maintainers must invite the intended team members, assign appropriate repository roles, protect `main` and `develop`, and configure required reviews and checks in GitHub settings. This document and the pull request template do not perform those account or repository-setting changes.
