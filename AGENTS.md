# negbeta.com AGENTS.md

Static one-page corporate marketing site for Negbeta Limited, deployed on Cloudflare Pages.

## Stack

- Hand-coded HTML/CSS in `public/`. No build step. No JavaScript.
- Deployed via `npx wrangler pages deploy`.

## Layout

- `public/index.html`: the home page (intro, products, company)
- `public/privacy/`, `public/terms/`, `public/404.html`: legal pages sharing the same header and footer
- `public/site.css`: styles (renamed from `styles.css` to bypass the edge cache; rename again on big changes)
- `public/fonts/host-grotesk-var.woff2`: the one self-hosted font
- `public/images/`: product stills
- `public/favicon.svg`, `public/robots.txt`, `public/sitemap.xml`
- `public/_headers`: Cloudflare Pages security headers
- `wrangler.toml`: Cloudflare Pages project config

## Bar

The site exists so payment processors, banks, and partners landing on `negbeta.com`
read it as a serious AI software company. Keep it confident-quiet:

- One family, Host Grotesk (self-hosted). Large tight headlines, small labels.
- Neutral paper (`#f2f2ee`), near-black ink, hairline rules. Colour only for product status
  (green dot for launching, outline dot for pending).
- Read like a real small startup: say what each product does for the people who use it, in
  plain words. No tech stack, vendors or infrastructure on the page. Legal disclosures stay in
  the footer. No eyebrow dots, no numbered "01 / 02" sections, no italic accent words,
  no gradients, no stock photos (product stills only), no JS, no analytics.
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
