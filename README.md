# homebrew-tap

```bash
brew install franzramadhan/tap/<app>
```

Every hour `.github/workflows/update.yml` checks the latest release of each
repository in `apps.txt` and, when it is newer than `Formula/<repo>.rb`,
regenerates that formula and commits it (signed, as github-actions[bot]). Run
the workflow by hand to update right after a release.

## Adding an app

1. The app repository publishes GitHub releases tagged `v<version>` with a
   `SHA256SUMS` asset.
2. It has `scripts/homebrew-formula.sh <version> <SHA256SUMS>`, which prints the
   formula on stdout (see franzramadhan/homie for an example).
3. Add `owner/repo` to `apps.txt`. No workflow change needed.
