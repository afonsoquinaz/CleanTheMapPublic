# Clean The Map — public site

The public pages for the Clean The Map iOS app (App Store listing links and
AdMob verification). The game's source lives in the private `CleanTheMap` repo.

| Page | URL (after GitHub Pages is on) |
|---|---|
| Marketing / home | https://afonsoquinaz.github.io/CleanTheMapPublic/ |
| Support URL | https://afonsoquinaz.github.io/CleanTheMapPublic/support.html |
| Privacy Policy URL | https://afonsoquinaz.github.io/CleanTheMapPublic/privacy.html |
| app-ads.txt | https://afonsoquinaz.github.io/CleanTheMapPublic/app-ads.txt |

## Turn the site on (once)
GitHub → this repo → **Settings → Pages** → Source: *Deploy from a branch*,
Branch: `main`, folder `/ (root)` → Save. The URLs above work a minute later.

## App Store Connect
App → **App Information**: Privacy Policy URL = the privacy page above.
Version page: Support URL = the support page, Marketing URL = the home page
(or your user site, see below). **App Privacy**: the game collects nothing
itself; declare what the Google Mobile Ads SDK collects (Identifiers →
Device ID, Usage Data → Advertising Data, Location → Coarse Location, all
used for Third-Party Advertising, linked to the user: No, tracking: Yes).

## app-ads.txt (AdMob "app-ads.txt not verified")
AdMob only accepts `app-ads.txt` at the **root of a domain** — the domain of the
*Marketing URL* (or developer website) in your App Store listing. A project page
like `afonsoquinaz.github.io/CleanTheMapPublic/` is a sub-folder, so for
verification use one of:

1. **GitHub user site (free):** a public repo named exactly
   `afonsoquinaz.github.io` with this `app-ads.txt` at its root and Pages on, and
   the App Store *Marketing URL* set to `https://afonsoquinaz.github.io`.
   All your apps share the same publisher line, so one file covers all of them
   (if that repo already exists for another game, nothing more is needed there).
2. **A custom domain** (e.g. `cleanthemap.com`) pointed at this repo
   (Settings → Pages → Custom domain); then `https://cleanthemap.com/app-ads.txt`
   is at the root. Set that domain as the Marketing URL.

Then AdMob → Apps → Clean The Map → **app-ads.txt → Check for updates**.
