# Contributor Onboarding Guide

Welcome to the team. This guide takes you from "I just got access" to "my first pull request is open." Work through it top to bottom; it should take under an hour.

If anything here is wrong or unclear, fixing this document is a perfectly good first contribution — see [Submitting a pull request](#6-submitting-a-pull-request).

## 1. Before you start

You will need:

- **A GitHub account** — create one at [github.com/signup](https://github.com/signup) if you don't have one, and turn on [two-factor authentication](https://docs.github.com/en/authentication/securing-your-account-with-two-factor-authentication-2fa).
- **Access to this repository** — ask a maintainer to add you to the organization if you can't clone.
- **The repository URL** — `https://github.com/mcpmark-eval-liuhezi/team-field-guide`
- **A terminal** and an editor you like. Any editor that previews Markdown will do.

## 2. Cloning the repository

Because you have been added to the organization, you can clone directly — no fork needed:

```bash
git clone https://github.com/mcpmark-eval-liuhezi/team-field-guide.git
cd team-field-guide
```

If you are contributing from **outside the organization**, fork the repository on GitHub, clone your fork, and add the upstream remote:

```bash
git clone https://github.com/YOUR-USERNAME/team-field-guide.git
cd team-field-guide
git remote add upstream https://github.com/mcpmark-eval-liuhezi/team-field-guide.git
```

Before starting any new work, make sure your local `main` is current:

```bash
git switch main
git pull origin main
```

> Never commit directly to `main`. Everything — including one-line fixes — arrives by pull request. See the house rules in the [README](../README.md).

## 3. Development environment setup

This is a documentation repository, so the toolchain is deliberately small:

1. **Git** — 2.30 or newer. Verify with `git --version`.
2. **An editor with Markdown preview** — VS Code works out of the box (`Cmd/Ctrl+Shift+V`), but any editor is fine.
3. **A Markdown linter (optional but recommended)** — keeps formatting consistent across contributors.

Verify your setup:

```bash
git --version          # prints a version, not an error
cat README.md          # you can read the seed files
```

Working habits that matter here:

- Write in **Markdown**, one topic per file under `docs/`.
- Keep lines reasonably short and prefer headings over long paragraphs.
- Commit in small units with messages that say *why*, not just *what*.

## 4. Where things live in the repo

The layout is sketched and maintained in [`docs/architecture.md`](architecture.md). The short version:

| Path | What it is | Read it when… |
| --- | --- | --- |
| `README.md` | The front door: what this repo is for, house rules, where to ask questions | …you're new, or you forget the rules |
| `CODE_OF_CONDUCT.md` | Our behavioral standards (Contributor Covenant) | …you want to know what's expected, or need to report something |
| `docs/architecture.md` | The intended repository layout and the reasoning behind it | …you're about to add or move a file |
| `docs/onboarding.md` | This guide | …it's your first day, or you're helping someone onboard |

When you add a file, update `docs/architecture.md` in the same pull request so the sketch never drifts from reality.

## 5. Making a change: branches

Every change starts from an issue. If there's no issue for what you want to do, open one — it's how the team sees what's in flight.

Then create a branch named after the work:

```bash
git switch -c docs/my-topic main
```

Branch naming convention: `area/short-description` — for example `docs/onboarding-guide` or `docs/code-of-conduct`.

Keep each branch to a single issue. Two unrelated fixes means two branches and two pull requests.

## 6. Submitting a pull request

When your change is ready:

```bash
git add docs/my-topic.md
git commit -m "Add my-topic guide"
git push -u origin docs/my-topic
```

Then open the pull request on GitHub against `main`. Two house rules apply to **every** PR, and a PR that misses either one will be sent back:

1. **The description must contain a `Closes #<issue number>` line.** This links the PR to its issue and closes the issue automatically when the PR merges. For example, if you're resolving issue 3, write:

   ```text
   Closes #3
   ```

   Put it on its own line so GitHub recognizes it.

2. **Every PR gets reviewed before it merges.** A reviewer leaves a comment starting with `Pre-merge check:` and only after that does the PR merge into `main`. Wait for it — don't merge your own PR unreviewed.

In the description, also say what changed and why, and link anything that gives the reviewer context.

## 7. After your PR merges

- Delete the branch — GitHub offers a button on the merged PR page.
- Sync your local `main`:

  ```bash
  git switch main
  git pull origin main
  git branch -d docs/my-topic
  ```

- Check that the linked issue closed automatically (it should have, thanks to the `Closes #` line). If it's still open, close it and say so in the issue.
- Pick up the next issue.

## 8. Where to ask questions

- **Anything about this guide or the repo** — open an [issue](https://github.com/mcpmark-eval-liuhezi/team-field-guide/issues). Ask in the open; the answer becomes searchable for the next person.
- **Something specific to a change** — comment on the pull request itself.
- **A problem with someone's conduct** — see [`CODE_OF_CONDUCT.md`](../CODE_OF_CONDUCT.md) for how to report it privately.

That's it — you're set up. Welcome aboard.
