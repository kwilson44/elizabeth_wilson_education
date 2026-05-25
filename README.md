# Elizabeth Wilson — Childcare & Education Professional

**Live site:** https://kwilson44.github.io/elizabeth_wilson_education

This repository contains Elizabeth Wilson's professional single-page portfolio showcasing her experience in babysitting, tutoring, and specialized childcare education. The site is hosted on GitHub Pages and includes:

- Responsive design with smooth scroll navigation
- Professional photography and credentials display
- Formspree contact form integration
- SEO optimization (OG tags, schema.org JSON-LD, sitemap, robots.txt)
- Google Search Console verified
- Print-friendly stylesheet
- Accessibility features (smooth scrolling, reveal animations)

## Quick local test

Serve the folder and open in a browser:

```bash
cd "/Users/katiewilson/Desktop/Ellie Surprise"
python3 -m http.server 8000
# open http://localhost:8000
```

## Current setup

- **Domain:** https://kwilson44.github.io/website
- **Contact:** stemgirl2000@gmail.com · (626) 314-0964
- **Location:** Rockville, MD
- **Google Search Console:** Verified ✓
- **Form backend:** Formspree (formId: xeedlqor)

## Updating content

### Contact info
Update in `index.html`:
- Email: search for `stemgirl2000@gmail.com`
- Phone: search for `(626) 314-0964`
- Also update the schema JSON-LD block in `<head>` with matching values

### Professional details
- **About section:** Edit the paragraph text under "A trusted presence for children and families"
- **Services:** Update the three service cards in the Services section
- **Credentials:** Edit or add credential items in the About section
- **Certifications:** Update the scrollable cert-list items
- **Reviews:** Edit testimonial quotes and reviewer names

### Photos
- `photo_one.jpg` — Hero card (professional headshot)
- `photo_two.jpg` — About section (action/teaching photo)
- `photo_three.jpg` — Certifications section (professional setting)
- `teaching_image.jpg` → favicon (also used for browser tab icon)

## Customizing the site

### Navigation & branding
- Site name: search for "Elizabeth Wilson, Jr." in `index.html`
- Nav links: edit href attributes in the `<nav>` element
- Footer: update copyright and author info

### Colors & styling
Edit CSS custom properties in the `<style>` block:
```css
:root {
  --cream: #FAF8F4;      /* Background */
  --sand: #F0ECE3;       /* Secondary background */
  --accent: #4A7C6F;     /* Primary accent (teal) */
  --dark: #1E1A17;       /* Text/dark elements */
  --warm-gray: #6B6560;  /* Secondary text */
}
```

### Formspree form
To change the contact form endpoint:
1. Create a new form at https://formspree.io
2. Copy the form ID
3. In `index.html`, find this line:
   ```js
   formspree('initForm', { formElement: '#contact-form', formId: 'xeedlqor' });
   ```
4. Replace `xeedlqor` with your new form ID

## SEO & search tools

### Google Search Console
- Property URL: https://kwilson44.github.io/website
- Meta verification: `<meta name="google-site-verification" content="...">` in `<head>`
- Sitemap: https://kwilson44.github.io/website/sitemap.xml
- Status: Currently verified ✓

### Schema markup
The site includes LocalBusiness schema JSON-LD. Update these fields in the `<head>`:
- `name`, `email`, `telephone`
- `address` (street, city, region, country)
- `url`, `geo` (latitude/longitude)
- `openingHours`, `priceRange`

### Sitemap & robots
- `robots.txt` — at site root
- `sitemap.xml` — at site root (update `lastmod` when making content changes)

## Commit & publish

After making changes, commit and push to GitHub:

```bash
git add .
git commit -m "Update [feature]: describe your changes"
git push
```

GitHub Pages publishes automatically; allow ~30–90 seconds for changes to appear on the live site.

## Features

- **Smooth scroll navigation** — Click nav links for smooth scrolling to sections
- **Active nav highlighting** — Current section is highlighted in the nav
- **Reveal on scroll** — Sections fade in as they enter the viewport
- **Responsive design** — Mobile-friendly layout
- **Print friendly** — Clean print stylesheet hides nav/form, optimizes for printing
- **Accessible forms** — Formspree AJAX with client-side validation
- **Favicon** — Custom favicon from teaching_image.jpg
- **Page load animation** — Subtle fade-up effect on page load

## Files & structure

```
.
├── index.html              # Main site (single-page)
├── favicon.ico             # Browser tab icon
├── robots.txt              # Search engine crawling rules
├── sitemap.xml             # XML sitemap for SEO
├── photo_one.jpg           # Hero card image
├── photo_two.jpg           # About section image
├── photo_three.jpg         # Certifications section image
├── teaching_image.jpg      # Original image (favicon source)
├── README.md               # This file
└── .venv/                  # Python virtual environment (local dev)
```

## Troubleshooting

**Site not updating after push?**
- Wait 1–2 minutes for GitHub Pages to rebuild
- Hard refresh browser (Cmd+Shift+R on Mac)
- Check that changes are actually committed and pushed

**Google Search Console verification failing?**
- Ensure the meta verification tag is in the `<head>` of published `index.html`
- Check that the property URL matches exactly
- Visit the live site URL and view page source to confirm the tag is visible

**Form not submitting?**
- Ensure Formspree is active and the formId is correct
- Check browser console for errors
- Test with a different email/browser if needed

**Images not showing?**
- Confirm photo files are in the repo root (same folder as index.html)
- Filenames are case-sensitive on GitHub Pages
- Push the images along with `index.html` changes

## Next steps

- Add Care.com or Nextdoor links to increase visibility
- Collect real testimonials and replace placeholder reviews
- Set up Google Analytics for traffic insights
- Consider adding a blog/updates section
- Expand certifications section with downloadable PDFs (if desired)
