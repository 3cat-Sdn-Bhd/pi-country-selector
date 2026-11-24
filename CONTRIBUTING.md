# Contributing

Owner: @buibaoanh

## Changes

- Pull requests only: no direct pushes, force pushes or deleting `main`. GitHub Free
  does not enforce this on private repositories.
- Get a review when another maintainer is available.
- `Secret scan` must pass.
- A committed credential must be rotated; deleting it leaves it in git history.

## Releasing

No deploy of its own: it is a Pi extension, loaded by whatever installs it from
this repository. A change on `main` ships when that consumer updates.
