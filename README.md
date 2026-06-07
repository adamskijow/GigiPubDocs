# Card Night At Gigi's — public docs

Support, privacy, and marketing pages for the App Store / Play / Steam release. This repo also hosts the pages for **All Fours in Ashes** under `ashes/` (see below).

Live at: https://adamskijow.github.io/GigiPubDocs/

- `index.html` — marketing landing (Apple **Marketing URL**)
- `support.html` — Apple **Support URL**
- `privacy.html` — **Privacy Policy URL**

## All Fours in Ashes (`ashes/`)

A second title's pages, in the `ashes/` subfolder. Same structure, its own folk-horror theme (`ashes/style.css`, `ashes/icon.svg`); no em dashes per that game's house style.

Live at: https://adamskijow.github.io/GigiPubDocs/ashes/

- `ashes/index.html`: marketing landing (Steam **Website URL**)
- `ashes/support.html`: Steam **Support URL**
- `ashes/privacy.html`: **Privacy Policy URL**

Steam store fields to paste:
- Website: `https://adamskijow.github.io/GigiPubDocs/ashes/`
- Support URL: `https://adamskijow.github.io/GigiPubDocs/ashes/support.html`
- Privacy Policy URL: `https://adamskijow.github.io/GigiPubDocs/ashes/privacy.html`

The Steam button on `ashes/index.html` still links to `#`; swap it for the real store URL once the app page is public. Not blocking; Steam only needs the support and privacy URLs above to resolve.

## First-time GitHub Pages setup

1. Push to `main`:
   ```bash
   git add .
   git commit -m "initial site"
   git push -u origin main
   ```
2. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch → main / (root) → Save**.
3. Wait ~1 minute, then verify:
   - https://adamskijow.github.io/GigiPubDocs/
   - https://adamskijow.github.io/GigiPubDocs/support.html
   - https://adamskijow.github.io/GigiPubDocs/privacy.html

## Updating

Edit, commit, push. Pages redeploys in under a minute.

## Before App Store submission

The three store buttons on `index.html` still link to `#`. Swap them for real store URLs once you have them. Not blocking — Apple only needs the three URLs above to resolve.
