# Card Night At Gigi's — public docs

Support, privacy, and marketing pages for the App Store / Play / Steam release.

Live at: https://adamskijow.github.io/GigiPubDocs/

- `index.html` — marketing landing (Apple **Marketing URL**)
- `support.html` — Apple **Support URL**
- `privacy.html` — **Privacy Policy URL**

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
