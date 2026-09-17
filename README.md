# Which Newsletter

Independent static site helping creators choose a newsletter platform: **beehiiv**, **Kit** (ConvertKit), **Ghost**, and **Substack**.

Live (GitHub Pages): https://tolmondh.github.io/which-newsletter/

## What’s in this repo

| Path | Purpose |
|------|---------|
| `index.html` | Home — value prop and links |
| `compare.html` | Pillar comparison matrix |
| `about.html` | Independence / about |
| `disclosure.html` | FTC-style affiliate disclosure |
| `guides/substack-to-beehiiv.html` | Migration guide outline |
| `guides/course-creators.html` | Fit guide for course creators |
| `styles.css` | Shared styles |
| `robots.txt` | Crawler rules + sitemap pointer |
| `sitemap.xml` | Absolute URLs for Pages |

Plain HTML + one CSS file. No build step, no npm, no framework.

## Base path (important)

This project is published as **GitHub Project Pages** under:

```text
https://tolmondh.github.io/which-newsletter/
```

All internal links and asset paths use the `/which-newsletter/` prefix (e.g. `/which-newsletter/styles.css`). Relative links from nested pages (e.g. `guides/`) would also work if rewritten — current pages use absolute-from-site-root paths with that base.

If you ever move the site to a custom domain at the root, update those paths (and `sitemap.xml` / canonicals).

## Enable GitHub Pages

1. Push this folder’s contents to a GitHub repo (e.g. `which-newsletter`) on branch `main`.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
4. Choose branch **`main`** and folder **`/ (root)`**.
5. Save. After a minute or two, the site is at `https://<user>.github.io/<repo>/`.

No GitHub Actions build is required for this static layout.

## Preview locally

From this directory:

```bash
# Python 3
python3 -m http.server 8080
```

Then open:

- Root-style preview: http://localhost:8080/  
- Path that matches Pages: serve the **parent** folder and open http://localhost:8080/which-newsletter/

Because CSS and nav use `/which-newsletter/...`, the second approach matches production. Example:

```bash
cd ..   # parent of which-newsletter-site
# Rename or symlink so the folder is named which-newsletter, then:
python3 -m http.server 8080
# Visit http://localhost:8080/which-newsletter/
```

Or temporarily replace `/which-newsletter/` with `/` in HTML/CSS for flat local preview (revert before publishing).

## Affiliates

CTA links for beehiiv, Kit, and Ghost use `href="#"` with `data-affiliate="beehiiv|kit|ghost"` and HTML comments marking where real partner URLs go. See `disclosure.html`.

## License / independence

Editorial site; not an official partner of the platforms named unless stated on the About page.
