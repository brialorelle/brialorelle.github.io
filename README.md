# brialong.com

Plain HTML/CSS rebuild of the old Wix site at www.brialong.com, for GitHub Pages. No build step:
edit the `.html` files directly.

- `style.css`: all styling (Lato from Google Fonts, teal from vislearnlab.org).
- `img/`: images copied from the Wix site.
- `_files/ugd/`: PDFs that were hosted on Wix, kept at the same path so old brialong.com PDF links keep working.
- `files/cv.pdf`: the CV page embeds this file. Replace it to update the CV.

## Preview locally

```bash
python3 -m http.server 8765
```

Then open http://localhost:8765.

## Pointing www.brialong.com here

1. Repo Settings → Pages → deploy from branch `main`, folder `/`.
2. Settings → Pages → Custom domain: `www.brialong.com` (GitHub adds a `CNAME` file).
3. At the domain registrar: a `CNAME` record for `www` → `brialorelle.github.io`, and `A` records for the apex
   `brialong.com` → 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153.
4. Once DNS resolves, tick "Enforce HTTPS".
