# homebrew-tap

```bash
brew install franzramadhan/tap/homie
```

`Formula/homie.rb` is written by `.github/workflows/update.yml`: every hour it
checks the latest [homie](https://github.com/franzramadhan/homie) release and,
when it is newer, regenerates the formula with homie's
`scripts/homebrew-formula.sh`. Run the workflow by hand to update right after a
release.
