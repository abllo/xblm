# xBloom Recipes Hub — Project Reference

## Overview
Arabic-language specialty coffee recipe platform.
- **Live site**: https://xblm.ab-s.me
- **GitHub**: github.com/abllo/xblm
- **Hosting**: GitHub Pages
- **Database**: Firebase Realtime Database (europe-west1)

---

## Firebase Configuration
- **Region**: europe-west1
- **DB URL**: https://xbloom-recipes-hub-default-rtdb.europe-west1.firebasedatabase.app
- **API Key**: AIzaSyDq370Yy4W-TfbyFL5rt4y3h3ngajJVIrE

---

## Design System
| Variable | Value |
|---|---|
| `--ta` | `#00A896` (accent / teal) |
| `--bg` | `#0A0A0A` (background) |
| `--card` | `#1A1A1A` (card background) |
| Gradient | `linear-gradient(135deg, #00A896, #4A90E2)` |

- Dark theme throughout
- RTL Arabic layout

---

## Key Files
| File | Purpose |
|---|---|
| `index.html` | Public-facing site |
| `admin.html` | Admin panel (password-protected) |
| `recipe.html` | Individual recipe page |
| `guides/` | SEO Arabic guide articles (10+ files) |
| `link-fixer.html` | Tool to repair corrupted Firebase link fields |

---

## Critical Rules — NEVER Break These

1. **All Firebase-dependent code must stay inside `<script type="module">`**
   - Never move Firebase logic outside the module script
   - `window.doLogin` inside a module is accessible to HTML `onclick` handlers ✓

2. **HTML banners must always load via `<iframe srcdoc>` with `sandbox` attribute**
   - Never inject banner HTML directly into the DOM

3. **Always deliver the complete modified file — never partial diffs or snippets**
   - User expects the full file every time, ready to copy-paste or push

4. **No new `<script>` tags outside the existing module script**
   - All new JS must live inside the existing `<script type="module">` block

---

## Field Labels (UI)
- `brewer` field → displayed as **"الفلتر"** everywhere (recipe card, share image, recipe.html)
  - NOT "الجهاز" — this label was chosen by the owner and must never change

---

## Architecture Notes
- 200+ recipes seeded from JS array into Firebase (no more dual-source)
- Admin panel uses SHA-256 password auth
- Sitemap: 209 URLs, submitted to Google Search Console
- Sitemap updater button in admin panel uses GitHub API
- Maintenance mode controlled via Firebase flag

---

## SEO Setup
- Schema.org markup ✓
- OG tags ✓
- Geo-targeting: Saudi Arabia ✓
- hreflang tags ✓
- Dynamic sitemap ✓

---

## Owner Preferences
- Language: Arabic (RTL)
- Location: Jeddah, Saudi Arabia
- Platform focus: Specialty coffee
- Style: Dark, refined, high-quality
- Delivery: Always full files, never partial code
