# Setup

Upload everything in this folder to the root of your `putheka/putheka` repository,
keeping the folder structure exactly as-is:

```
putheka/
├── README.md
├── assets/
│   └── banner.svg
└── .github/
    └── workflows/
        ├── metrics.yml
        └── snake.yml
```

## 1. Add the token

The metrics workflow needs a token to read your contribution data.

1. github.com/settings/tokens → **Generate new token (classic)**
2. Tick the **`repo`** scope. Copy the token.
3. In `putheka/putheka`: **Settings → Secrets and variables → Actions → New repository secret**
4. Name it exactly `ACCESS_TOKEN`. Paste the token as the value.

Without this the metrics workflow fails and `assets/metrics.svg` never appears.

## 2. Run both workflows once

They're on daily schedules, so the first run must be manual:

**Actions** tab → **generate metrics** → **Run workflow** → wait for green tick.
It takes 1–3 minutes and commits two SVGs into `assets/`.
Then the same for **generate snake**.

After that, refresh your profile. All images should render.

## Uploading via the web UI

GitHub's drag-and-drop upload will not include `.github/` — the browser hides
dotfolders. Either:

- **Use git** (recommended):
  ```bash
  git clone https://github.com/putheka/putheka.git
  # copy these files in, keeping structure
  git add -A && git commit -m "profile readme" && git push
  ```
- **Or create the workflows by hand**: on the repo page, **Add file → Create new
  file**, type `.github/workflows/metrics.yml` as the filename (the slashes
  create the folders), paste the contents. Repeat for `snake.yml`.

## Troubleshooting

**Metrics images broken.** Check the Actions run log. Almost always a missing or
expired `ACCESS_TOKEN`, or the token lacks `repo` scope. The workflow commits
`assets/metrics.svg` and `assets/activity.svg` — if those files aren't in the
repo after a green run, the commit step was blocked (see workflow permissions
below).

**Snake image broken.** Confirm an `output` branch now exists in the repo and
contains `snake.svg`. If the workflow succeeded but the branch is empty, the
`GITHUB_TOKEN` write permission was denied — check
**Settings → Actions → General → Workflow permissions** is set to
*Read and write*.

**Banner broken.** The path is relative (`./assets/banner.svg`), so it only
fails if the file isn't at `assets/banner.svg` in the repo root.

**Workflow permissions.** Both workflows write to the repo.
**Settings → Actions → General → Workflow permissions** must be
*Read and write permissions*. This is the second most common cause of a
green run that produces no files.

## Last thing

The three `pinned` tiles at the bottom are placeholders. Replace them with real
repository names and one honest line each about what the project solves. That
section is the only part of this profile a reader can't get from anyone else's.
