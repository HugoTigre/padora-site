# Padora website (GitHub Pages)

Static site for Play Store privacy policy and a minimal landing page.

**Source of truth:** this folder in the `padora` repo. Publish to a separate **public** repo for GitHub Pages (the main app repo stays private).

## Publish to `padora-site`

```sh
# One-time: create public repo on GitHub (empty, no README)
# https://github.com/new → name: padora-site → Public

cd website
git init
git add .
git commit -m "Initial Padora site (privacy policy + landing)"
git branch -M main
git remote add origin git@github.com:HugoTigre/padora-site.git
git push -u origin main
```

## Enable GitHub Pages

1. GitHub → **padora-site** → **Settings** → **Pages**
2. **Source:** Deploy from branch **main**, folder **/ (root)**
3. Save — site goes live at `https://hugotigre.github.io/padora-site/`

**Play Console privacy policy URL:**

`https://hugotigre.github.io/padora-site/privacy.html`

## Changing the URL later

When you move to `padora.app` (or Firebase / GCP hosting), update the URL in **Play Console → App content → Privacy policy**. Old GitHub Pages URLs can redirect or stay as a fallback until you remove them.

## Updating content

Edit files here, then from `website/`:

```sh
git add .
git commit -m "Update privacy policy"
git push
```

Or re-copy changed files into your `padora-site` clone and push.
