# tesskern.com

Personal site of Tess Kern, Ph.D. student in Crop Sciences at the University of Illinois Urbana-Champaign: quantitative genetics, plant breeding, and crop modeling.

Live at <https://tesskern.com>.

## Editing

The whole site is one file, `index.html`, with the styles and script inline. Edit it and push to `main`. Cloudflare deploys the change in about a minute.

Other files:

- `favicon.svg`: browser tab icon.
- `og-image.png`: the preview image shown when the link is shared.
- `sitemap.xml` and `robots.txt`: help search engines find the site. Update `<lastmod>` in `sitemap.xml` after big changes.
- `wrangler.toml` and `.assetsignore`: Cloudflare settings. Anything listed in `.assetsignore` is not published.

## Blog (paused)

The blog is turned off for now. Its source (`blog-src/`) and built files (`blog/`) are kept in the repo. To bring it back, remove the two `blog` lines from `.assetsignore`, add a Blog link to the nav in `index.html`, and see `BLOG.md`.
