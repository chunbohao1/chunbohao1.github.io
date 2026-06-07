# Chunbo Hao — Academic Homepage

Personal academic homepage built with [Hugo](https://gohugo.io/).  
Live site: [https://chunbohao1.github.io](https://chunbohao1.github.io)

## Features

- **Hugo static site** — fast builds, no Ruby/Jekyll dependency
- **Responsive layout** — sidebar profile + main content, mobile-friendly
- **Publications** — card layout with venue tags, first-author / co-author sections
- **GitHub Pages** — build locally with Hugo, deploy manually

## Project Structure

```
├── config.toml              # Site config (title, author, menu, params)
├── content/
│   └── _index.md            # Homepage content (about, education, papers, projects)
├── layouts/
│   ├── _default/baseof.html
│   ├── index.html
│   └── partials/            # masthead, sidebar, google_scholar_stats
├── static/
│   ├── css/main.css
│   └── images/avatar.png    # Profile photo & favicon
├── run_server.sh            # Local dev server
```

## Quick Start

### 1. Clone & install Hugo

```bash
git clone https://github.com/chunbohao1/chunbohao1.github.io.git
cd chunbohao1.github.io

# Install Hugo Extended (example on Ubuntu)
sudo apt install hugo
```

### 2. Configure

Edit `config.toml`:

| Key | Description |
|-----|-------------|
| `title` | Your name |
| `params.description` | Bio shown in sidebar |
| `params.avatar` | Avatar path (`images/avatar.png`) |
| `params.email` / `googleScholar` / `dblp` / `orcid` | Contact & academic links |
| `params.repository` | `USERNAME/REPO` (for Scholar stats CDN, if used) |
| `[menu.main]` | Top navigation anchors |

Replace `static/images/avatar.png` with your own photo.

### 3. Edit content

Main page content lives in `content/_index.md`:

- About Me, Research Area
- Education (`edu-card`)
- Publications (`paper-card`, grouped by first / co-author)
- Open Source Projects

Paper citation badges on the page can use:

```html
<span class='show_paper_citations' data='PAPER_ID'></span>
```

`PAPER_ID` is the Google Scholar `citation_for_view` ID from the paper URL.

### 4. Deploy to GitHub Pages

Build locally, then push the `public/` output to the `gh-pages` branch:

```bash
hugo --minify
cd public
git init
git add -A
git commit -m "Deploy site"
git push -f git@github.com:chunbohao1/chunbohao1.github.io.git main:gh-pages
```

In repo **Settings → Pages**, set source to branch **`gh-pages`** / **`/ (root)`**.

Source code (Hugo project) stays on `main`; only built HTML goes to `gh-pages`.

## Local Development

```bash
bash run_server.sh
```

Open [http://localhost:4000](http://localhost:4000). Hugo watches `content/`, `layouts/`, `static/`, and `config.toml` for changes.

Build production site manually:

```bash
hugo --minify
# output in public/
```

## Acknowledgments

- Originally based on [AcadHomepage](https://github.com/RayeRen/acad-homepage.github.io) (Jekyll / Minimal Mistakes)
- [Font Awesome](https://fontawesome.com/) — icons (SIL OFL 1.1 / MIT)
- [Academicons](https://jpswalsh.github.io/academicons/) — academic icons
