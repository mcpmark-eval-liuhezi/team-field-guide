# Architecture

> Status: **sketch**. This file describes the intended layout of `team-field-guide`. As the guide grows, update this sketch in the same PR that introduces the change.

## Purpose

This repository is documentation-only. It exists so that one authoritative place holds our onboarding material, working agreements, and conduct standards.

## Intended layout

```text
team-field-guide/
├── README.md              # Entry point: purpose, audience, house rules, where to ask
├── CODE_OF_CONDUCT.md     # Contributor Covenant — behavioral standards
└── docs/
    ├── architecture.md    # This file — the layout of the guide itself
    └── onboarding.md      # Day-one path for a new contributor
```

### `README.md`

The front door. Covers what the repo is for, who it's for, the PR house rules, and where to ask questions. It should stay short and point into `docs/` for anything longer than a few paragraphs.

### `docs/`

Long-form, topic-specific guides. A new guide means a new file here, plus a line in this layout sketch:

- `architecture.md` — this file.
- `onboarding.md` — the contributor onboarding guide: cloning, environment setup, where things live, and submitting a PR.

Future additions that this layout anticipates:

- `docs/reviewing.md` — how we review, what "done" means for a review.
- `docs/glossary.md` — team vocabulary and acronyms.
- `docs/repository-index.md` — pointers to the product repositories this team maintains.

### `CODE_OF_CONDUCT.md`

Lives at the repository root so GitHub surfaces it automatically. Based on the Contributor Covenant.

## Conventions that hold this together

- Documentation is written in Markdown, one topic per file under `docs/`.
- Each document begins with a short purpose statement so a reader knows within ten seconds whether the file is for them.
- Every change — including to this file — arrives via pull request referencing an issue (`Closes #<n>`), receives a `Pre-merge check:` review, and only then merges to `main`.

## Evolution

When the layout changes, keep this page in sync in the same PR. If a file listed here disappears, remove it from the sketch; if a new file appears, add it with a one-line description.
