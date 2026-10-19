# devadharshini97.github.io

Personal academic site. Plain HTML/CSS/JS, no build step.

## Deploy on GitHub Pages

1. Rename the repo `devadharshini97/devadharshini.github.io` to **`devadharshini97.github.io`**
   (Settings → General → Repository name). The site then lives at `https://devadharshini97.github.io/`
   instead of the longer `/devadharshini.github.io/` path.
2. Keep the old Jekyll site on a branch first: `git checkout -b old-academicpages && git push -u origin old-academicpages`.
3. Back on `master`, delete the old files and copy in this folder (`index.html`, `assets/`, `README.md`, `.nojekyll`).
4. Commit and push. In Settings → Pages, set Source to "Deploy from a branch", branch `master`, folder `/ (root)`.

`.nojekyll` tells GitHub Pages to serve the files as-is, without running Jekyll.

## Editing

Everything is in `index.html`. Each research/project entry is an `<article class="row">` block: copy one and edit it.

### Replacing thumbnails with your results

The SVGs in `assets/thumbs/` are interim illustrations. Replace them with real results:

- Still image: put a 320×200 (16:10) image in `assets/thumbs/` and change the `<img src>`.
- Hover video (Barron style): add a short muted clip next to the image. It plays while the row is hovered:
  ```html
  <div class="thumb">
    <img src="assets/thumbs/deform.jpg" alt="...">
    <video src="assets/media/deform.mp4" muted loop playsinline preload="none" aria-hidden="true"></video>
  </div>
  ```
  Keep clips to 3–6 s and under ~2 MB:
  `ffmpeg -i in.mp4 -t 5 -vf "scale=-2:240,fps=24" -an -c:v libx264 -crf 28 -pix_fmt yuv420p -movflags +faststart out.mp4`

### Portrait

`assets/profile.jpg` (square). The page redraws it as 2D Gaussians on load and on hover.
Users with reduced motion turned on see the photo directly.

### CV

Replace `assets/Devadharshini_Ayyappan_CV.pdf` whenever the resume changes.
