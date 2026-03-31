Portfolio static site

Status: Ready for static hosting (GitHub Pages / Netlify / Vercel).

Notes:
- Canonical entry: `index.html` (keeps full site). `portfolio.html` now redirects to `index.html` to avoid duplicate content.
- Assets: `styles.css`, `compressed.png` are present in repository root.
- The site uses React via CDN and Babel (JSX transpiled in-browser). This is fine for small personal sites but not recommended for high-traffic production.

Quick local test (recommended):
- Using Python (if installed):

```powershell
python -m http.server 8000
# Open http://localhost:8000 in your browser
```

- Using Node.js `serve` (if Node installed):

```powershell
npx serve . -l 8000
# Open http://localhost:8000
```

Deploy options:
- GitHub Pages: push repo, ensure branch `main` (or `gh-pages`) used and enable Pages to serve from root.
- Netlify: connect repository or drag-and-drop the repo folder into Netlify; publish directory is root `/`.
- Vercel: connect repo and deploy; root will serve `index.html`.

Optional improvements:
- Precompile JSX and bundle with a build tool (Vite/Parcel) for production performance.
- Remove unused duplicate files (`app.js`, `script.js`, `data.js`) or convert them into a single external bundle.
- Add analytics, sitemap, and meta tags for SEO.
