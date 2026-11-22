# matchlight.fi

Public website for Matchlight. Plain static HTML and CSS, no build step, hosted on GitHub Pages.

## Structure

```
index.html        Landing page
privacy.html      Privacy notice for the website
404.html          Not found page
CNAME             Custom domain for GitHub Pages (matchlight.fi)
favicon.svg       From claude/brand/matchlight-favicon.svg
robots.txt, sitemap.xml
assets/
  site.css
  brand/          F2 logo (horizontal, cropped viewBox), profile icon,
                  apple-touch-icon.png (180 px) and og-image.png (1200x630)
  fonts/          Inter Tight, self-hosted (SIL OFL, see OFL-LICENSE.txt)
```

## Rules

- No cookies, analytics or third-party requests. Fonts are self-hosted on purpose (GDPR).
- Brand rules live in the project doc "VARUMÄRKE, LOGGA OCH INSTAGRAM". No gradients, no emojis, no promises about features that do not work yet.
- UI text in English. Brand colors: graphite #121417, bone #F4F1EA, orange #F04E14, yellow #FFB627.
- Changes go through a branch and pull request. `main` is what is live.

## Local preview

```
python3 -m http.server 8000
```

Open http://localhost:8000.

## Deploy

GitHub Pages: Settings → Pages → Deploy from a branch → `main` / root. Custom domain `matchlight.fi`, Enforce HTTPS on.

## DNS (Hostingpalvelu, zone matchlight.fi)

| Name | Type | Value |
|---|---|---|
| matchlight.fi | A | 185.199.108.153 |
| matchlight.fi | A | 185.199.109.153 |
| matchlight.fi | A | 185.199.110.153 |
| matchlight.fi | A | 185.199.111.153 |
| www | CNAME | matchlightfinland.github.io |

Do not touch the MX record or `mail.matchlight.fi`. Email depends on them.
