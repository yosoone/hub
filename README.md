# hub.yoso.one

Yoso's hub page: one static page linking to the vault, paintings, photography, short texts, Mastodon, the mailing list and RSS feeds.

## Sites

| Site | Address | Content |
|---|---|---|
| The Vault | [one.yoso.one](https://one.yoso.one) | Notes on Buddhism, Shinto, meditation, kokoro and Japan (Obsidian Publish) |
| Kuro | [kuro.yoso.one](https://kuro.yoso.one) | Black-and-white photography of Japan |
| Shinsei | [shinsei.yoso.one](https://shinsei.yoso.one) | Sumi-e paintings and hanging scrolls |
| River | [river.yoso.one](https://river.yoso.one) | Short texts |
| Mastodon | [@Yosoone](https://mastodon.social/@Yosoone) | Day-to-day notes |

## Files

- `index.html`: the whole page (HTML and CSS in one file; fonts from Google Fonts)
- `CNAME`: serves the site at `hub.yoso.one`
- `.nojekyll`: publishes the files as they are, without a Jekyll build
- `archive/feed.html`: the earlier Mastodon and Ghost feed page

## Hosting

1. **Settings → Pages → Build and deployment**: *Deploy from a branch*, branch `main`, folder `/ (root)`.
2. At the DNS provider for `yoso.one`, add a `CNAME` record: name `hub`, value `yosoone.github.io`.
3. Once the domain resolves, tick **Enforce HTTPS** in the Pages settings.

## To do

- [ ] Mailing-list signup URL (`#mailing-list` placeholder in `index.html`)
- [ ] Confirm the RSS feed address for each site

## Safety: check, publish, undo

**Before publishing**, run the check in this folder:

```
python3 check.py
```

It looks for broken HTML, links to missing files, script errors, a missing hub link or mailing-list form, and a broken `feed.xml` or `robots.txt`. GitHub runs the same check on every push ('Check and publish' under the Actions tab). Once Settings → Pages → Source is set to **GitHub Actions**, a version that fails the check is never published: the live site keeps its last good version, and GitHub emails you what went wrong.

**To undo the last change**, in this folder:

```
git revert HEAD
git push
```

**To go back to a known-good version** (kept as branches named `good-YYYY-MM-DD`):

```
git fetch origin
git checkout origin/good-2026-10-20 -- .
git commit -m "Back to the good version of 20 October 2026"
git push
```

A full copy of this site, with its history, is also backed up to the external drive (`BLACK_PUNK_/00 Yoso_one Websites Back up`).
