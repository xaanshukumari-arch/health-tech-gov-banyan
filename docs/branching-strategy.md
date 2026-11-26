# Git Branching Strategy

## Branch roles

- **`main`** is the stable branch. Changes reach it through a reviewed release pull request from `develop`; do not commit directly to it.
- **`develop`** is the integration branch for completed feature work. It should remain buildable and is the target for feature pull requests.
- **Feature branches** hold one focused change and are created from `develop`.

## Feature workflow

1. Start from an up-to-date `develop` branch.
2. Create a branch named `feature/<issue-number>-<short-description>`, for example `feature/5-branching-strategy`.
3. Keep the change focused, commit related work, and push the feature branch to GitHub.
4. Open a pull request from the feature branch into `develop`. Link the relevant issue and describe the change and how it was checked.
5. Address review feedback and wait for required checks and approvals before merging.
6. Delete the feature branch after it has been merged.

## Releases

When the integration changes are ready for a release, open a pull request from `develop` into `main`. Review the changes and verify required checks before merging. Keep `main` as the stable reference point.

## Repository settings

Protect `main` and `develop` against direct pushes where repository permissions allow. Require pull requests, appropriate approvals, and passing automated checks before merging. These protections must be configured in GitHub; this document does not apply the settings.
