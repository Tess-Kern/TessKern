# Blog

The blog is a Quarto project. Source lives in `blog-src/`, and the rendered site goes to `blog/`, which is served at <https://tesskern.com/blog/>.

## Add a post

1. Create a folder for the post: `blog-src/posts/my-new-post/`
2. Add `index.qmd` to it:

   ````markdown
   ---
   title: "My new post"
   description: "One-line summary for the listing page."
   date: 2026-11-15
   categories: [R]
   ---

   Some text.

   ```{r}
   plot(cars)
   ```
   ````

   Images or data files the post uses go in the same folder.

3. Render from inside `blog-src/`:

   ```powershell
   cd blog-src
   quarto render
   ```

   To preview with live reload while writing, run `quarto preview` instead.

4. Commit and push. Include `blog-src/`, `blog-src/_freeze/` and `blog/`:

   ```powershell
   git add blog-src blog
   git commit -m "Add post: My new post"
   git push
   ```

   Pushing to `main` deploys the site.

## Notes

- **Freeze:** `execute: freeze: auto` means a post's R code re-runs only when that post's `.qmd` changes. The saved results are kept in `blog-src/_freeze/`. Commit that folder so old posts never need re-running.
- **Stop local servers before rendering:** on Windows, a running `wrangler dev` locks files in `blog/`, and Quarto then silently fails to copy plot images into it. Stop the server, run `quarto render`, then start the server again.
- **Drafts:** add `draft: true` to a post's front matter to keep it out of the listing.
- **Theme:** the colors and fonts in `blog-src/custom.scss` (light) and `custom-dark.scss` (dark) mirror the CSS variables in `index.html`. If you change the homepage palette, update them too.
- **If `quarto` isn't found:** Quarto is currently the copy bundled with RStudio and isn't on PATH. Either add `C:\Program Files\RStudio\resources\app\bin\quarto\bin` to PATH, or install Quarto from <https://quarto.org>. If Quarto can't find R, set `$env:QUARTO_R = "C:\Program Files\R\R-4.5.2\bin"` first.
