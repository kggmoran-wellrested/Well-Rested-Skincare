# Project: Well Rested Skincare
Last updated: 2026-03-07

## What This Project Is
Well Rested Skincare is a static HTML affiliate site that reviews and directories 24 science-backed skincare brands and at-home devices. It is monetized via affiliate links (Amazon Associates, Sovrn, Impact Radius). There is no backend — all files are plain HTML/CSS/JS.

## Tech Stack
- **Frontend:** Plain HTML/CSS/JS — no framework
- **Hosting:** GitHub Pages
- **Build process:** None — static files deployed directly
- **Version control:** GitHub — repo: github.com/kggmoran-wellrested/well-rested-skincare
- **Analytics:** Google Analytics 4 — Measurement ID: G-H93DL9R9QJ
- **Affiliate networks:** Amazon Associates, Sovrn, Impact Radius
- **Commission rates:** 3–10% depending on product/network

## File Structure
```
well-rested-skincare/
├── CLAUDE.md
├── index.html
├── brand-directory.html
├── brand-page.html               ← Dynamic template: brand-page.html?brand=[slug]
├── editorial.html
├── about.html
├── affiliate-disclosure.html
├── article-am-routine.html
├── article-actives.html
├── article-devices.html
├── robots.txt
├── sitemap.xml
├── llms.txt
├── googlec46f137391f8e5a2.html   ← Google Search Console verification — do not delete
├── CNAME
└── images/
    └── products/                 ← 47 product images (.webp format, informal filenames)
```

> **Note on article structure:** Articles currently live in the root. When article count reaches 6+, migrate to an `/articles/` subfolder and update sitemap + internal links accordingly.

## Replication Pattern
When creating a new page, always use `index.html` as the base template. Copy its full `<head>` section (including GA4, meta tags, and canonical), update the values for the new page, then build the body content. Never start a new `.html` file from scratch.

## Conventions & Rules
- ALWAYS add the GA4 tracking snippet to any new `.html` page created (Measurement ID: G-H93DL9R9QJ)
- ALWAYS add schema markup when creating new brand or article pages
- ALWAYS add a unique `<title>`, `<meta name="description">`, and `<link rel="canonical">` to every page
- NEVER link to pages that don't exist yet
- NEVER use inline styles — CSS goes in `<style>` blocks in the `<head>` of each file (no separate CSS files currently)
- Meta descriptions must be under 160 characters
- All affiliate links must include `rel="nofollow sponsored noopener"` and target="_blank"
- Brand page URL pattern: `brand-page.html?brand=[slug]`
- Article URL pattern: `article-[slug].html` (root folder until 6+ articles exist)
- Image path: `images/products/[filename].webp`
- Product image filenames use informal naming (e.g. `cerave cleanser.webp`) — always check actual GitHub filenames before referencing

## Brand Slugs (all 24)
**Skincare:** alastin, biossance, cerave, drunk-elephant, elemis, la-roche-posay, obagi, paulas-choice, plated, prequel, sk-ii, skinceuticals, summer-fridays, supergoop, tata-harper, tower28, zo

**Devices:** dr-pen, jovs, maysama, myolift, nira, nuderma, ziip

## Current SEO State
- sitemap.xml: ✅ exists and submitted to Google Search Console
- robots.txt: ✅ exists (AI crawlers allowed)
- llms.txt: ✅ exists
- Google Search Console: ✅ verified (March 7, 2026)
- GA4: ⏳ property not yet created — Measurement ID ready: G-H93DL9R9QJ
- Pages indexed by Google: pending (submitted March 7, 2026)

## Known Issues / Active Work
- [ ] GA4 tracking snippet not yet added to any pages (do all at once when confirmed)
- [ ] Organization schema not yet added to index.html
- [ ] article-actives.html missing updated meta tags and schema (not yet sent through SEO update pass)
- [ ] index.html missing updated meta tags, OG tags, and schema
- [ ] about.html missing updated meta tags
- [ ] affiliate-disclosure.html missing updated meta tags
- [ ] Individual brand pages rely on dynamic template (brand-page.html?brand=[slug]) — no static per-brand URLs yet, which limits SEO ranking per brand
- [ ] Sitemap does not yet include article-devices.html entry — needs update
- [x] robots.txt created and deployed (March 7, 2026)
- [x] sitemap.xml created and submitted (March 7, 2026)
- [x] llms.txt created and deployed (March 7, 2026)
- [x] Meta tags + schema added to: brand-directory.html, brand-page.html, article-am-routine.html, article-devices.html
- [x] Google Search Console verified (March 7, 2026)
- [x] 47 product images uploaded to images/products/
- [x] brand-page.html dynamic template built and working
- [x] editorial.html updated with devices article card (live)

## Affiliate & Business Context
- Affiliate networks: Amazon Associates, Sovrn, Impact Radius
- Disclosure page: /affiliate-disclosure.html
- Paid placements policy: None — editorial independence maintained ("0 Paid Placements")
- Commission structure: 3–10% depending on product and network
- Amazon Associates status: pending approval (need 3 sales within 180 days)
- LLC: Well Rested LLC — application submitted, pending approval
- Instagram: @wellrestedskincare

## Do Not Touch
- Do not edit the affiliate disclosure legal language in affiliate-disclosure.html
- Do not change the color scheme or typography (DM Serif Display, DM Mono, DM Sans — teal #3D7A7A)
- Do not remove the "0 Paid Placements" stat from the homepage
- Do not delete googlec46f137391f8e5a2.html — this is the Google Search Console verification file
- Do not rename or move product images in images/products/ without updating brand-page.html references
