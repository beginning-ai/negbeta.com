# negbeta.com AGENTS.md

Static one-page corporate marketing site for Negbeta Limited, deployed on Cloudflare Pages.

## Stack

- Hand-coded HTML/CSS in `public/`. No build step. No JavaScript.
- Deployed via `npx wrangler pages deploy`.

## Layout

- `public/index.html`: the entire site
- `public/style.css`: styles
- `public/favicon.svg`, `public/robots.txt`, `public/sitemap.xml`
- `public/_headers`: Cloudflare Pages security headers
- `wrangler.toml`: Cloudflare Pages project config

## Bar

The site exists so payment processors, banks, and partners landing on `negbeta.com`
read it as a serious AI software company. Keep it confident-quiet:

- Typography is the design (Fraunces display, IBM Plex Sans body).
- Off-white background, off-black ink, one warm accent (oxblood).
- No stock photos, no gradients-as-backgrounds, no JS, no analytics.
- Mobile-first responsive from 360px upward.
- Lighthouse Performance and Accessibility ≥ 95.

## Disclosures

Footer carries Companies Act 2006 s.1202 disclosures (legal name, company
number, registered office). Any change to the registered office must
update the footer in the same change.

## Version control

This repo uses `jj` colocated with `git`. Use `jj` commands locally; the
git remote is `git@github.com:beginning-ai/negbeta.com`.

## Deploy

```sh
npx wrangler pages deploy public --project-name=negbeta-com --branch=main
```

The custom domain `negbeta.com` is bound to the Pages project in the
Cloudflare dashboard.
