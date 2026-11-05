# Personalized Fork — Omnitrix Network (Free-Telegram-Proxy)

This repository is a personalized fork of
[0xRadikal/Free-Telegram-Proxy](https://github.com/0xRadikal/Free-Telegram-Proxy)
(MIT). The brand was changed from **Raydikalx** to **Omnitrix Network**, and the
repository now points at the **aMyNaR** fork:

- Telegram channel: `@Omnitrix_Network` — https://t.me/Omnitrix_Network
- GitHub: https://github.com/aMyNaR/Free-Telegram-Proxy
- Live dashboard (after Pages is enabled): https://amynar.github.io/Free-Telegram-Proxy/

Removed: `@configexBot`, the sister-project promo (Free-v2ray-Configs), the
donation section and `.github/FUNDING.yml`. The channel QR was regenerated
(`assets/readme/qr-channel.svg`). All data/GitHub/dashboard URLs in templates,
docs, code and tests now reference the fork.

Test suite: `tests/test_readme.py` and `tests/test_site.py` pass (89/89); the
full suite passes 264/266 — the 2 remaining errors are a Windows-only path-length
issue in `test_hostile_nested_json_does_not_crash` (unrelated to this rebrand;
they pass on the Linux CI).

## Still required

1. **Brand images** — `docs/assets/brand-icon.webp`, `docs/assets/brand-hero*.webp`,
   `docs/favicon.png`, `docs/assets/social-preview.png`, `docs/assets/apple-touch-icon.png`
   still contain the old logo. Replace them with Omnitrix assets (any square icon
   works for `brand-icon`); keep file names so the HTML loads them.
2. **Subscriber badge** — the shields.io endpoint uses `tg.sumanjay.workers.dev/Omnitrix_Network`.
   Verify it resolves; if it does not, remove that badge line from the three templates
   (and the generated READMEs).
3. **GitHub settings (outside code)** — enable Actions on the fork (the update
   workflow runs every ~15 min and publishes lists), enable Pages from `docs/`,
   and set the repo About/description/website.

## Publishing note

The bot regenerates `README.md` / `README_FA.md` / `README_RU.md` from
`templates/` on every run — always edit the templates first.
