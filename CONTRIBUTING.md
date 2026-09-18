# Contributing

Thanks for contributing. This is the org-wide default — GitHub renders it in
every repository that lacks its own `CONTRIBUTING.md`. A repository only
carries its own file when its flow genuinely diverges (and says why at the
top).

## Workflow (GitHub Flow)

- `main` is always deployable.
- Every change lands via a short-lived branch off `main`:
  `feat/<slug>`, `fix/<slug>`, `chore/<slug>`, `docs/<slug>` — the type
  matches the Conventional Commit type.
- Open a PR when the branch is ready (draft early for visibility). The PR is
  the integration point: CI must be green before merge.
- Merge style: **squash** — one commit per change/use case on `main`. Delete
  the branch after merge.
- Never push directly to `main`. Exception: a repository's initial scaffold.

## Commits

Conventional Commits: `<type>(<scope>): <description>` — imperative,
lowercase, ≤ ~72 chars. Collapse by feature before pushing: the history
tells the story of where it landed, not the journey.

## Labels

The Shape Up set: `type: slice`, `type: pitch`, `type: task`, `type: bug`,
`type: chore`.

## For agents

- Ask before commit/push/PR.
- Never force-push, never rewrite pushed history, never commit secrets.
- Tests ship in the same change as the code (TDD).
