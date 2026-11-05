# Personalized Fork — Omnitrix Network (Free-Telegram-Proxy)

This repository is a personalized fork of
[0xRadikal/Free-Telegram-Proxy](https://github.com/0xRadikal/Free-Telegram-Proxy)
(MIT). The brand was changed from **Raydikalx** to **Omnitrix Network**:

- Telegram channel: `@Omnitrix_Network` — https://t.me/Omnitrix_Network
- `@configexBot`, the sister-project promo (Free-v2ray-Configs), the donation
  section and `.github/FUNDING.yml` were removed.
- All READMEs (templates + generated copies), the dashboard (`docs/`), SVG
  assets, support files and tests were updated; the QR for the channel was
  regenerated (`assets/readme/qr-channel.svg`).
- Test suite: `tests/test_readme.py` and `tests/test_site.py` pass (89/89);
  the full suite passes 264/266 — the 2 remaining errors are a Windows-only
  path-length issue in `test_hostile_nested_json_does_not_crash` (unrelated to
  this rebrand; they pass on the Linux CI).

## Still required (needs your input)

1. **GitHub URLs** — point to your fork (the "Star" card, the dashboard
   "GitHub" links, JSON-LD `canonical`/`sameAs`, and `SUPPORT.md` links still
   reference the upstream repo). Replace `https://github.com/0xRadikal/Free-Telegram-Proxy`
   with your repository URL in:
   - `templates/README.md`, `templates/README_FA.md`, `templates/README_RU.md`
     (and the generated `README*.md` copies)
   - `docs/index.html`, `docs/fa/index.html` (header/footer/nav links)
   - `docs/data/index.html`, `docs/fa/data/index.html`, `docs/methodology/index.html`,
     `docs/fa/methodology/index.html` (header links, JSON-LD)
   - `tests/test_readme.py` (`_GROW["star"]`)
   - `.github/ISSUE_TEMPLATE/config.yml` (Q&A links)
2. **Live dashboard URL** — the old `0xradikal.github.io/...` links still point to
   the upstream dashboard. After you enable GitHub Pages on your fork, replace
   them with your own Pages URL (e.g. `https://<you>.github.io/Free-Telegram-Proxy/`).
3. **Brand images** — `docs/assets/brand-icon.webp`, `docs/assets/brand-hero*.webp`,
   `docs/favicon.png`, `docs/assets/social-preview.png`, `docs/assets/apple-touch-icon.png`
   still contain the old logo. Replace them with Omnitrix assets (any square
   icon works for `brand-icon`); keep file names for the HTML to load them.
4. **Subscriber badge** — the shields.io endpoint uses `tg.sumanjay.workers.dev/Omnitrix_Network`.
   Verify it resolves; if it does not, remove that badge line from the three templates
   (and the generated READMEs).
5. **GitHub settings (outside code)** — enable Actions on the fork (the update
   workflow runs every ~15 min and publishes lists), enable Pages from `docs/`,
   and update the repo About/description/website.

## Publishing note

The bot regenerates `README.md` / `README_FA.md` / `README_RU.md` from
`templates/` on every run — always edit the templates first.
