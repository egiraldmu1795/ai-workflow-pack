# AI Automation Workflow Pack — Sales Page

Static GitHub Pages-ready landing page. No build step required.

## Deploy

Push the `site/` directory to any static host (GitHub Pages, Netlify, Cloudflare Pages). The `.nojekyll` file tells GitHub Pages to skip Jekyll processing.

## TODO before going live

1. **Buy buttons** — search for `<!-- TODO: Gumroad URL -->` in `index.html`. There are 4 `href="#"` anchors with `data-buy` attributes (`templates` and `starter-kit`). Replace each `href="#"` with the actual Gumroad product URL once the products are created in your Gumroad account.

2. **OG image** — update the `og:image` meta tag to the real hosted image URL.

3. **SRI hash on Tailwind CDN** — the Tailwind CDN `<script>` tag currently has no `integrity` attribute. For a hardened production page, pin a specific Tailwind CDN version and add an `integrity="sha384-..."` + `crossorigin="anonymous"` attribute. For a quick launch this is low risk (Tailwind CDN is widely trusted), but worth hardening before high-traffic campaigns.

4. **Contact email** — the footer links to `egiraldmu@gmail.com`. Replace with a dedicated support address if preferred.

## Structure

```
site/
  index.html   — self-contained page (Tailwind via CDN, inline JS)
  .nojekyll    — disables Jekyll on GitHub Pages
  README.md    — this file
```
