# Sean's Wishlist

Static wishlist page for GitHub Pages. Content lives in `index.md`; dark/light mode follows the device setting (dark by default styling, mobile-first).

## Setup

1. Create a GitHub repo and push this folder to `main`.
2. Repo **Settings → Pages → Build and deployment → Source: GitHub Actions**.
3. If this is a project site (`https://USER.github.io/REPO`), set `baseurl: "/REPO"` in `_config.yml`. Leave it empty for a `USER.github.io` repo.
4. Every push to `main` redeploys via `.github/workflows/pages.yml`.

## Releases

```sh
git tag v1.0.0
git push origin v1.0.0
```

`.github/workflows/release.yml` builds the site and attaches `wishlist-site-<tag>.zip` (rendered HTML) and `wishlist-source-<tag>.zip` to a GitHub Release.

## Editing

Edit `index.md` (plain Markdown lists, one item per bullet). Styling is in `assets/css/style.css`.

Preview locally (optional): `gem install jekyll && jekyll serve`.
