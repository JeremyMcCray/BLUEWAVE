# Blue Wave Election Night Tracker 2026

A static, dependency-free election tracker (one `index.html` + one `data.js`). No build step.

## Deploy to GitHub Pages

1. Create a repo and push this folder to the `main` branch.
2. In the repo go to **Settings → Pages** and set **Source** to **GitHub Actions** (not "Deploy from a branch").
3. The `Deploy to GitHub Pages` workflow runs on every push to `main` (or manually from the Actions tab) and publishes the site at `https://<user>.github.io/<repo>/`.

## Updating results

All race data lives in `data.js` — one object per race, documented at the top of the file. Edit, commit, push; the workflow redeploys in about a minute. Update `window.LAST_UPDATE` in the same file so the timestamps on the page match.

Fields: `n` name · `o` office · `lvl` Senate/House/Governor/Ballot · `st` state · `reg` region · `s` win/loss/run · `p` vote % · `r` % reporting · `flip` · `date` M/D · `note`.
