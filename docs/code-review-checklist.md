# Code Review Checklist

Use this checklist for pull requests before merging:

## Scope and correctness

- Confirm the change addresses the linked issue and is limited to the intended scope.
- Check the implementation for correctness, error handling, and relevant edge cases.
- Review tests or other validation evidence; request targeted checks when behavior is not covered.

## Security and privacy

- Check that no credentials, secrets, or real patient information are included in source, tests, or logs.
- Review access-control and data-handling changes for least privilege and data minimisation.
- Confirm errors and logs do not unnecessarily expose sensitive information.

## Maintainability and readiness

- Check that names, structure, and patterns are consistent with the project.
- Confirm user-facing or operational documentation is updated when needed.
- Leave specific, actionable comments for requested changes, and record approval only when blocking concerns are resolved.

The assigned reviewer should be someone other than the pull request author. Merge only after required approvals and automated checks pass. Repository owners must configure required reviewers and checks in GitHub settings; this checklist alone does not enforce them.
