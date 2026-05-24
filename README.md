# Elizabeth Wilson — Website

This repository contains a single-page site (index.html) for Elizabeth Wilson, a childcare & education professional. The site is set up for GitHub Pages and includes Formspree integration, basic SEO (OG/meta tags), schema.org JSON-LD, a sitemap, and robots.txt.

## Quick local test

Serve the folder and open in a browser:

```bash
cd "/Users/katiewilson/Desktop/Ellie Surprise"
python3 -m http.server 8000
# open http://localhost:8000
```

## Replace Google Search Console verification

1. Go to https://search.google.com/search-console and add property (URL prefix): `https://kwilson44.github.io/website`.
2. Google will provide a verification meta tag like:

```html
<meta name="google-site-verification" content="YOUR_TOKEN_HERE" />
```

3. Open `index.html` and replace the placeholder token (`abc123xyz`) with the token Google gives you.
4. Commit and push:

```bash
git add index.html
git commit -m "Add Google Search Console verification"
git push
```

5. Wait ~1 minute for GitHub Pages to update, then click `Verify` in Search Console.

## Submit sitemap

Sitemap URL: `https://kwilson44.github.io/website/sitemap.xml`

After verification, open Search Console → Sitemaps and submit that URL.

## Edit contact, profile, and SEO

- Visible name / nav / footer: edit `index.html` (search for `Elizabeth Wilson` or the elements: `.nav-logo`, `.hero-card-name`, footer span).
- Contact email: update the email shown in the contact area (search for `ellie.wilson@email.com`).
- Formspree: to change the form endpoint, edit the init call near the bottom of `index.html`:

```js
formspree('initForm', { formElement: '#contact-form', formId: 'xeedlqor' });
```

Replace `xeedlqor` with the new Formspree formId if needed.

- Open Graph & meta tags: update the tags in the `<head>`.
- Schema (JSON-LD): edit the `<script type="application/ld+json">` block in the `<head>` to update `name`, `telephone`, `email`, `address`, and `url`.

## robots.txt & sitemap

Files are at the site root:
- `robots.txt`
- `sitemap.xml`

These are already present; update `sitemap.xml` `lastmod` if you make content changes.

## Commit & publish

```bash
git add .
git commit -m "Update site content and SEO"
git push
```

GitHub Pages will publish automatically from the repository; allow ~30–90 seconds for changes to propagate.

## Troubleshooting

- If verification fails, ensure the meta tag is present in the published `index.html` at the exact GitHub Pages URL.
- Use the browser to open `https://kwilson44.github.io/website/index.html` (or the root) to confirm the meta tag is visible in page source.

## Next steps (optional)

- Replace the Google verification token (I can do that if you paste it here).
- Provide final contact info (email, phone) and I will embed it into `index.html` and the JSON-LD.
- Add per-section reveal timing/stagger or additional microcopy changes.

If you want me to do any of the next steps, tell me which and I'll implement them.