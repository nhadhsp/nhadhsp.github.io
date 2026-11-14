# Nha Tran – Academic Homepage

Static personal website (HTML + CSS, no JavaScript), layout adapted from Jon Barron's template.

## Folder structure

```
index.html              page content (bio, papers, teaching)
style.css               all styles: colors, fonts, layout, light/dark mode
images/photo.jpg        profile photo
images/papers/*.jpg     one model figure per paper
```

## Publish on GitHub Pages

1. Create a public repository named `<your-github-username>.github.io`.
2. Upload every file and folder above, keeping the same structure.
3. Open **Settings → Pages**, set *Source* to `Deploy from a branch`, branch `main`, folder `/ (root)`.
4. After 1–2 minutes the site is live at `https://<your-github-username>.github.io`.

## Common edits

**Add a paper**: in `index.html`, copy one `<article class="pub">…</article>` block, paste it in the right place (newest first), then change:

- the image path `images/papers/<name>.jpg` (put the figure in `images/papers/`)
- the title and its link (DOI)
- the author list
- the venue line; the small badge is `<span class="tag">Q1</span>` (delete it if not needed)

A paper without a figure can keep one of the drawn thumbnails, for example
`<div class="thumb"><svg viewBox="0 0 160 120" aria-hidden="true"><use href="#s-attention"/></svg></div>`.

**Change the photo**: replace `images/photo.jpg` with a square image (about 480×480 px).

**Change colors or sizes**: edit the variables at the top of `style.css`
(`--link` = link color, `--bg` = background, `--text` = text color). The second block of
variables is used in dark mode.

**Thumbnail size**: `.thumb { width: 200px; height: 130px; }` and `.pub { grid-template-columns: 200px 1fr; }` in `style.css`.
