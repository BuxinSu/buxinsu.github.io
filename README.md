# Buxin Su — Personal Website

A self-contained static website (plain HTML + CSS, no build step, no external
dependencies or fonts). Works on any static host, including GitHub Pages.

## Structure

```
index.html          Home — bio, Recent & Featured Papers, News & Awards
publications.html   Full publication list (journals, conferences, preprints)
talks.html          Invited talks
service.html        Professional service
assets/style.css    All styling (light + dark mode, responsive)
assets/buxin-su.jpg Profile photo
assets/Buxin_Su_CV.pdf  CV linked from the nav bar
```

## Deploying to GitHub Pages

1. Create a **new repository on your own GitHub account** named
   `<your-username>.github.io` (e.g. `buxinsu.github.io`).
2. Put the contents of this `website/` folder at the repository root
   (i.e. `index.html` at the top level) and push:

   ```bash
   cd website
   git init
   git add .
   git commit -m "Personal website"
   git branch -M main
   git remote add origin git@github.com:<your-username>/<your-username>.github.io.git
   git push -u origin main
   ```

3. The site will appear at `https://<your-username>.github.io` within a few
   minutes. (For a `*.github.io` repository, GitHub Pages is enabled
   automatically from the `main` branch; if not, enable it under
   *Settings → Pages → Deploy from a branch → main*.)

## Updating content

- **New paper**: copy an existing `<li class="pub">…</li>` block in
  `publications.html` (and `index.html` if featured) and edit the
  title/authors/venue/links.
- **News item**: copy an existing `<li>` in the News & Awards list in
  `index.html`. Newest entries go on top.
- **New CV**: replace `assets/Buxin_Su_CV.pdf` with the new file (same name).
- **Photo**: replace `assets/buxin-su.jpg` (same name).
- **Accent color**: edit the `--accent*` variables at the top of
  `assets/style.css`.
