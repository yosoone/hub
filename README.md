# hub.yoso.one

Yoso's hub page: one static page linking to the vault, photography, short texts, Mastodon, the mailing list and RSS feeds.

## Sites

| Site | Address | Content |
|---|---|---|
| The Vault | [one.yoso.one](https://one.yoso.one) | Notes on Buddhism, Shinto, meditation, kokoro and Japan |
| Kuro | [kuro.yoso.one](https://kuro.yoso.one) | Black-and-white photography of Japan |
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
