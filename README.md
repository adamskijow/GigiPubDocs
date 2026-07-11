# Joey Beans Games — public site

The web home for **Joey Beans Games LLC** and its titles. Hosted on GitHub Pages.

- **Live:** https://adamskijow.github.io/GigiPubDocs/
- **Planned custom domain:** https://joeybeansgames.com/ — after DNS is configured

## Structure

```
/                     Studio landing page (Joey Beans Games LLC)
  index.html
  style.css
  icon.svg
  support.html        redirect stub -> gigi/support.html (legacy Apple URL)
  privacy.html        redirect stub -> gigi/privacy.html (legacy Apple URL)

/gigi/                Card Night At Gigi's (App Store / Play / Steam)
  index.html          Apple Marketing URL
  support.html        Apple Support URL
  privacy.html        Privacy Policy URL

/ashes/               All Fours in Ashes (Steam)
  index.html          Steam Website URL
  support.html        Steam Support URL
  privacy.html        Privacy Policy URL
```

The redirect stubs at the root keep the old `…/support.html` and `…/privacy.html`
links working, since *Card Night* moved into `gigi/`.

## Store fields to use

**Card Night At Gigi's** (update these in App Store Connect / Play / Steam):
- Marketing / Website: `https://joeybeansgames.com/gigi/`
- Support URL: `https://joeybeansgames.com/gigi/support.html`
- Privacy Policy URL: `https://joeybeansgames.com/gigi/privacy.html`

**All Fours in Ashes** (Steam):
- Website: `https://joeybeansgames.com/ashes/`
- Support URL: `https://joeybeansgames.com/ashes/support.html`
- Privacy Policy URL: `https://joeybeansgames.com/ashes/privacy.html`

The Steam buttons use the titles' public Steam URLs. Add App Store and Google
Play buttons to `gigi/index.html` only after their final public URLs are known.

## Connecting the custom domain (one-time)

The domain is registered on Cloudflare. GitHub Pages allows **one custom domain per
repo** — this repo serves `joeybeansgames.com`.

**1. Cloudflare → DNS.** Add these records and set every one to **DNS only (grey
cloud), not Proxied (orange)** — the orange proxy blocks GitHub's TLS certificate:

| Type  | Name | Value                    |
|-------|------|--------------------------|
| A     | `@`  | `185.199.108.153`        |
| A     | `@`  | `185.199.109.153`        |
| A     | `@`  | `185.199.110.153`        |
| A     | `@`  | `185.199.111.153`        |
| CNAME | `www`| `adamskijow.github.io`   |

**2. Add a `CNAME` file** containing `joeybeansgames.com`, commit it, and push.

**3. GitHub → repo Settings → Pages.** Confirm **Custom domain** reads
`joeybeansgames.com`. Wait ~15–60 min for the DNS check and certificate, then
tick **Enforce HTTPS**.

**4. (Optional) Verify the domain** under GitHub account Settings → Pages to prevent
takeover.

## Updating

Edit, commit, push to `main`. GitHub Pages redeploys in under a minute.
