# AxyProxy Switcher — Website

Landing page, privacy policy, and Chrome Web Store assets for **AxyProxy Switcher** — a proxy profile manager for Chrome, forked and hardened from [SwitchyOmega](https://github.com/FelisCatus/SwitchyOmega).

**Live site:** https://axyproxy-site.pages.dev  
**Extension repo:** https://github.com/vnetmx/SwitchyOmega

---

## Contents

```
index.html                          # Full landing page + privacy policy (single file, zero deps)
favicon.svg                         # SVG favicon
_redirects                          # Cloudflare Pages redirect rules (/privacy → /#privacy)
store-assets/
  icon-128.png                      # Chrome Web Store extension icon (128×128)
  promo-small-440x280.png           # Small promotional tile (440×280)
  promo-large-920x680.png           # Large promotional tile (920×680)
  promo-marquee-1400x560.png        # Marquee promotional tile (1400×560)
```

## Page sections

| Section | Description |
|---------|-------------|
| **Hero** | Extension name, tagline, install CTA, trust badges |
| **Features** | 9-card grid covering all major capabilities |
| **How it works** | 4-step visual flow |
| **Open source** | Attribution strip with GitHub link |
| **Privacy Policy** | Full Chrome Web Store compliant policy |

## Chrome Web Store assets

| Asset | File | Size |
|-------|------|------|
| Store icon | `store-assets/icon-128.png` | 128×128 |
| Small promo tile | `store-assets/promo-small-440x280.png` | 440×280 |
| Large promo tile | `store-assets/promo-large-920x680.png` | 920×680 |
| Marquee promo tile | `store-assets/promo-marquee-1400x560.png` | 1400×560 |

**Privacy policy URL** (required in CWS dashboard → Privacy practices):
```
https://axyproxy-site.pages.dev/#privacy
```

## Deployment

The site is deployed on **Cloudflare Pages** via direct upload using Wrangler:

```bash
CLOUDFLARE_ACCOUNT_ID=<account-id> \
CLOUDFLARE_API_TOKEN=$(secret get cloudflare_token) \
wrangler pages deploy . --project-name axyproxy-site --branch main --commit-dirty=true
```

To connect via Git instead:
1. Go to [Cloudflare Pages dashboard](https://dash.cloudflare.com/?to=/:account/pages) → **Create a project**
2. Connect to `vnetmx/axyproxy-site`
3. Framework preset: **None** · Build command: *(empty)* · Output directory: *(empty)*
4. Deploy

## License

Site content © 2025 Alejandro Mendez.  
Extension is a fork of [SwitchyOmega](https://github.com/FelisCatus/SwitchyOmega) © 2012–2017 The SwitchyOmega Authors. Licensed under [GPL-3.0](https://www.gnu.org/licenses/gpl-3.0.html).
