# Maintaining trq.io

The landing page **is** `README.md`. Edit it on github.com (pencil icon),
commit, and trq.io rebuilds in about a minute.

## What each file does

| File | Purpose |
|---|---|
| `README.md` | The page itself. Jekyll renders it as the site index. |
| `_config.yml` | Site title, tagline and theme (`jekyll-theme-cayman`). |
| `_includes/head-custom.html` | OG/Twitter cards, favicon, theme color. |
| `CNAME` | Binds the Pages site to `trq.io`. Do not delete. |
| `logo.png` | Referenced by the OG image tag. |

## DNS (Cloudflare, DNS-only)

| Type | Name | Value |
|---|---|---|
| A | `@` | 185.199.108.153 |
| A | `@` | 185.199.109.153 |
| A | `@` | 185.199.110.153 |
| A | `@` | 185.199.111.153 |
| CNAME | `www` | `trq-io.github.io` |

Proxy status must be **DNS only** (grey cloud) so GitHub can issue the
Let's Encrypt certificate. Enforce HTTPS in Settings → Pages once the cert
is issued.

## Preview locally (optional)

```bash
bundle exec jekyll serve
```

Needs a `Gemfile` with `gem "github-pages", group: :jekyll_plugins`. Not
required — pushing to `main` is the real preview.
