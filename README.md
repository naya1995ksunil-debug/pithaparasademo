# Pitha Pasara — Deploy to GitHub Pages

This repo has one file that matters: **`index.html`**. It's a complete,
self-contained website (React + styling + your logo, all inlined) that loads
its few dependencies from public CDNs at runtime — so GitHub Pages can serve
it with zero build step.

## Deploy it (takes about 2 minutes)

1. **Create a new repository on GitHub**
   Go to [github.com/new](https://github.com/new), name it something like
   `pitha-pasara`, keep it **Public** (required for free GitHub Pages), and
   click **Create repository**. Don't initialize it with a README — you
   already have these files.

2. **Push these files to it**
   In this folder, run:
   ```bash
   git init
   git add .
   git commit -m "Pitha Pasara storefront"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/pitha-pasara.git
   git push -u origin main
   ```
   Replace `YOUR-USERNAME` with your actual GitHub username.

   (No `git` installed, or prefer not to use the command line? On the repo
   page, click **Add file → Upload files**, drag in `index.html` and
   `.nojekyll`, and commit directly in the browser.)

3. **Turn on GitHub Pages**
   In the repo, go to **Settings → Pages**. Under "Build and deployment",
   set **Source** to **Deploy from a branch**, branch **main**, folder
   **/ (root)**. Click **Save**.

4. **Visit your site**
   GitHub will give you a URL like:
   ```
   https://YOUR-USERNAME.github.io/pitha-pasara/
   ```
   It usually goes live within a minute or two of saving the Pages setting.

## What's `.nojekyll` for?

GitHub Pages runs your site through Jekyll by default, which can interfere
with files/folders starting with an underscore. This project doesn't have
any, but it's a harmless, standard safeguard — keep it.

## Using your own domain later

If you buy a domain (e.g. `pithapasara.com`), add a `CNAME` file in this
folder containing just the domain name, then point your domain's DNS at
GitHub Pages. GitHub's guide:
https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

## Updating the site later

Edit `index.html` (or ask Claude for changes and drop in the new version),
then:
```bash
git add index.html
git commit -m "Update site"
git push
```
GitHub Pages redeploys automatically within a minute or two.
