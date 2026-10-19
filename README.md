# team-field-guide

Welcome to the **team-field-guide** — the single source of truth for how this team works. It is the first thing a new teammate should read, and the place we go back to whenever we forget how something is supposed to be done.

## What this repo is for

This repository holds the team's written practices:

- **Onboarding** — everything a new contributor needs on day one: cloning, environment setup, repo layout, and how to open a pull request.
- **Architecture notes** — a sketch of how the repository is organized and why.
- **Conduct** — the standards of behavior we hold ourselves to (see `CODE_OF_CONDUCT.md`).
- **Working agreements** — branch, PR, and review conventions that all changes follow.

It is deliberately documentation-only. Product code lives in its own repositories; this guide tells you where those are and how to work in them.

## Who this repo is for

- **New teammates** — start with `docs/onboarding.md` and work top to bottom.
- **Existing contributors** — when you need the canonical answer to "how do we do X around here?"
- **Reviewers and maintainers** — the PR house rules described below apply to every change, no exceptions.

## How we work: the house rules for changes

1. The seed commit on `main` contains the README and `docs/architecture.md`. **Nothing else is ever pushed directly to `main`.**
2. Every change arrives by **pull request** from its own feature branch.
3. Every PR description must contain a line of the form `Closes #<issue number>` so the linked issue closes automatically on merge.
4. Every PR receives at least one **review comment beginning with `Pre-merge check:`** before it is merged.

## Where to ask questions

- **Anything about onboarding or these docs** — open a [GitHub issue](https://github.com/mcpmark-eval-liuhezi/team-field-guide/issues) on this repository.
- **Stuck on a PR or a review is unclear** — comment directly on the pull request in question.
- **Time-sensitive or blocked** — raise it in the team channel and link the relevant issue or PR.

Questions asked in the open (issues and PRs) are better than questions asked in private, because the answer becomes searchable for the next person.

## Repository layout at a glance

See [`docs/architecture.md`](docs/architecture.md) for the intended layout and the reasoning behind it.
