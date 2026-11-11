# tesskern.com

Personal site of Tess Kern, Ph.D. student in Crop Sciences at the University of Illinois Urbana-Champaign. The site focuses on quantitative genetics, plant breeding, and crop modeling.

Live at <https://tesskern.com>.

## About

This repository contains the source for the personal website of Tess Kern, including:

- research and academic profile
- professional background
- crop modeling and quantitative genetics interests
- blog content archive (currently paused)

## Editing

The site is built as a single-page HTML site. The main content and styling live in `index.html`, with inline CSS and JavaScript.

After making changes, push to `main`. Cloudflare deploys the site automatically in roughly one minute.

## Repository contents

- `index.html`: main site content and styling
- `favicon.svg`: browser tab icon
- `og-image.png`: preview image used for social sharing
- `sitemap.xml`: sitemap for search engines
- `robots.txt`: crawler instructions
- `wrangler.toml`: Cloudflare deployment configuration
- `.assetsignore`: files excluded from the published site
- `blog-src/`: source files for the blog
- `blog/`: built blog output

## Blog status

The blog is currently paused. The source files remain in `blog-src/`, and the built output remains in `blog/`.

To reactivate the blog:

1. Remove the `blog` entries from `.assetsignore`
2. Add a Blog link to the site navigation
3. Rebuild/publish the site

## Deployment

This site is deployed with Cloudflare. Changes are published from the repository's `main` branch.
