# kendibah-web

The website for [Kendibah](https://kendibah.com): the root page, the privacy policy and the
terms of service. Static HTML with no build step.

## Hosting

- **kendibah.com** is served by Cloudflare Pages from `main`, output directory `/`, with no
  build command. Merging to `main` publishes the site.
- `https://kendibah.com/` is the App Store support and marketing URL, so the root page must
  always link to a contact address. `privacy.html` and `terms.html` are linked from the app
  (`LegalURLs` in `xoloUno/kendibah-app`) and from the App Store metadata. Don't rename or move
  them.
- The app's links change host only through `scripts/update-legal-urls.sh` in kendibah-app.

## Files

- `index.html`: support and legal links (Contact, Privacy, Terms)
- `privacy.html`, `terms.html`: the legal pages

## Adding the marketing page

The landing page replaces `index.html` in this repo, and its footer carries the Contact,
Privacy and Terms links. If it's built in Kickstart, follow the export-and-patch checklist in
the archived `xoloUno/flara-web` README, and don't overwrite `privacy.html` or `terms.html`
with the export's copies.
