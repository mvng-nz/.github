# Contributing

These are the working conventions for MVNG Consulting repositories. They apply to internal team members and any outside collaborators we invite onto an engagement.

## Branching

We use a trunk-based / GitHub-flow model:

- `main` is always deployable and protected — no direct pushes.
- Branch off `main` for every change. Naming: `type/short-description`
  - `feat/payment-reconciliation`
  - `fix/timezone-offset`
  - `chore/bump-deps`
- Keep branches short-lived. Open a draft PR early if you want feedback.

## Commits

Use [Conventional Commits](https://www.conventionalcommits.org/):

```
feat(api): add idempotency key to payment endpoint
fix(auth): handle expired refresh token
docs(readme): clarify local setup
```

This keeps history readable and lets us automate changelogs later.

## Pull requests

- Every change goes through a PR. At least **one review** is required before merge.
- All status checks must pass.
- Keep PRs focused — easier to review, safer to revert.
- Fill in the PR template, including the security checklist.
- **Never commit secrets.** Use environment variables / a secrets manager. Push protection is enabled org-wide, but treat it as a backstop, not a substitute for care.

## Code review

Reviews are about the code, not the person. Reviewers: be specific and constructive. Authors: respond to every comment, even if just to acknowledge. Prefer "disagree and commit" over stalling — escalate to an owner if genuinely blocked.

## Local setup

Each repository documents its own setup in its README. If something's missing or wrong, fix the README in the same PR.
