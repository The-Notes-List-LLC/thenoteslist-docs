# The Notes List — user guide source

Markdown source for [The Notes List](https://thenoteslist.com) user guide.

This repository is **synced bi-directionally with GitBook**. Edits made in the
GitBook editor are committed here automatically, and commits pushed here appear
in GitBook. GitBook is the day-to-day authoring surface; this repo is the
durable source of truth and the build input for the guide as rendered on
thenoteslist.com.

## Why this repo is separate from the app

The application repo's `main` branch is protected — it requires a pull request
and passing CI before anything lands. GitBook's Git Sync pushes commits
**directly** to its configured branch and does not open pull requests, so it
cannot target a protected branch. Keeping the guide here means the writer can
publish without a PR gate on every typo, and without the app's CI running on
prose changes.

It is public deliberately. The guide is public content, and a public repo means
the site build can read it with no token, no deploy key, and no private
submodule handling on Vercel.

## Do not put anything sensitive here

No credentials, no customer data, no internal notes. This repo is public and its
contents are published on the website.

## Rendering

Content here is rendered as **markdown**, not MDX. MDX compiles to executable
JavaScript; this repository is written to by an external editor, so compiling it
would let repo contents execute during the site build. Markdown rendering has no
such path. Keep it that way.

## Conventions

- One page per markdown file.
- Headings drive the on-page table of contents, so keep the hierarchy sane —
  a single `#` per page, `##` for sections.
- Images live alongside the pages that use them.
