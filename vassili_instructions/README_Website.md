# Personal Website with al-folio + GitHub Pages

Target: a live site at `https://<username>.github.io`, editable locally with Docker.

Verified against al-folio `v1.0` (June 2026).

---

## Part 1 — Setup & Deploy

### 1. Create your repo from the template

Go to <https://github.com/alshedivat/al-folio> → green **Use this template** → **Create a new repository**.

> Use the template button, **not** Fork. A fork stays linked to the upstream project and makes it easy to accidentally open PRs against it.

Name it:

| Site type | Repo name | Resulting URL |
|---|---|---|
| Personal / org | `<username>.github.io` | `https://<username>.github.io` |
| Project | anything, e.g. `lab-site` | `https://<username>.github.io/lab-site/` |

Keep it **public** (private repos need GitHub Pro for Pages).

### 2. Grant Actions write permission

Repo → **Settings** → **Actions** → **General** → **Workflow permissions** → select **Read and write permissions** → **Save**.

Without this, the deploy workflow cannot push the built site.

### 3. Configure `_config.yml`

Edit in the GitHub web UI (pencil icon) and commit:

```yaml
title: My Website
first_name: Your
last_name: Name
url: https://<username>.github.io
baseurl:            # personal site: leave EMPTY, do not delete the key
# baseurl: /lab-site/   # project site: use this instead
```

`url` has no trailing slash. `baseurl` for a project site has both slashes.

### 4. Wait for the deploy workflow

Repo → **Actions** tab → the **Deploy site** run should finish green (~4 min).

If it fails, the cause is almost always step 2.

### 5. Point Pages at the built branch

Repo → **Settings** → **Pages**:

- **Source**: `Deploy from a branch`
- **Branch**: `gh-pages` — **not** `main` — folder `/ (root)`
- **Save**

The workflow creates and owns `gh-pages`. Never commit to it by hand.

### 6. Verify

Wait ~1 min for `pages-build-deployment` to finish, then open your URL.

### 7. Clone for local work

```bash
git clone https://github.com/<username>/<repo-name>.git
cd <repo-name>
```

Every push to `main` triggers a rebuild automatically. No manual deploy step.

### 8. Files you will actually edit

| Path | Purpose |
|---|---|
| `_config.yml` | Site-wide settings, theme color, feature toggles |
| `_pages/about.md` | Landing page / bio |
| `assets/img/prof_pic.jpg` | Profile photo (replace, keep the filename) |
| `_bibliography/papers.bib` | Publications (BibTeX in, page out) |
| `_data/socials.yml` | Social + academic links |
| `_news/` | Short announcements shown on the homepage |
| `_projects/` | Project cards |
| `_posts/` | Blog posts, named `YYYY-MM-DD-title.md` |

### 9. Field-by-field reference

Two rules that apply everywhere:

- **YAML is indentation-sensitive.** Two spaces per level, spaces only, never tabs. A stray indent breaks the build.
- **`_config.yml` changes need a rebuild.** Restart the container (or re-push). Everything else hot-reloads.

#### `_config.yml`

Identity — drives the navbar name, `<title>`, and SEO:

```yaml
title: blank              # navbar brand; "blank" falls back to your name
first_name: Ada
middle_name:
last_name: Lovelace
description: >            # site-wide meta description
  Postdoc in numerical analysis at ...
keywords: numerical analysis, scientific computing
```

Publication author matching — underlines *your* name in the publication list. Include every form your name appears in:

```yaml
scholar:
  last_name: [Lovelace]
  first_name: [Ada, A., A. B.]
```

Feature toggles — search for these keys and flip them:

| Key | Effect |
|---|---|
| `search_enabled` | Site-wide search (navbar button + `Ctrl/Cmd+K`) |
| `bib_search` | Search box on the publications page |
| `posts_in_search` / `socials_in_search` | Include posts / social links in search results |
| `enable_darkmode` | Light/dark toggle |
| `enable_navbar_social` | Social icons in the navbar, not just the about page |
| `enable_project_categories` | Category tabs on the projects page |
| `enable_publication_thumbnails` | Show `preview` images next to publications |
| `max_author_limit` | Authors shown before a "more" link; blank = show all |
| `enable_medium_zoom` | Click-to-zoom on images |
| `enable_progressbar` | Scroll progress bar |

Layout:

```yaml
max_width: 930px          # content column width
navbar_fixed: true        # navbar sticks on scroll
footer_fixed: true
back_to_top: true
```

Removing sections — **exclude rather than delete**. Deleting causes merge conflicts on future upgrades:

```yaml
exclude:
  - _pages/blog.md
  - _posts/
  - _projects/
```

#### `_pages/about.md`

This is your landing page. Front matter controls the layout, body is plain Markdown:

```yaml
---
layout: about
title: about
permalink: /                # keep as / — this is the homepage
subtitle: <a href='#'>Lab or Department</a>. Office. Email.

profile:
  align: right              # right | left
  image: prof_pic.jpg       # filename inside assets/img/
  image_circular: false     # true = circular crop
  more_info: >              # HTML block under the photo
    <p>Room 4021</p>
    <p>Montréal, QC</p>

selected_papers: true       # show papers marked selected={true}
social: true                # social icons at the bottom
announcements:
  enabled: true
  scrollable: true
  limit: 5                  # news items shown
latest_posts:
  enabled: true
  limit: 3
---

Your bio goes here, in Markdown.
```

Set any of `selected_papers`, `social`, `announcements.enabled`, `latest_posts.enabled` to `false` to hide that block.

Other pages in `_pages/` use `nav: true` and `nav_order: 3` to control whether and where they appear in the navbar.

#### `assets/img/prof_pic.jpg`

Simplest path: replace the file, keep the name. Otherwise drop your image in `assets/img/` and point `profile.image` at the new filename. Square, ~800×800, under ~500 KB.

#### `_data/socials.yml`

One key per line, uncomment what you use, delete or leave blank what you don't. **Display order follows file order.**

```yaml
email: ada@university.ca
github_username: adalovelace
scholar_userid: XXXXXXXXXXXX     # from your Scholar profile URL
orcid_id: 0000-0002-1825-0097
linkedin_username: adalovelace
work_url: https://lab.university.ca
```

Most IDs are the bare identifier, not a full URL — the plugin builds the link. `work_url` is the exception. The file's own comments list every supported key; anything not there can be added via a `custom_social` block with `title`, `url`, and `logo`.

#### `_bibliography/papers.bib`

Standard BibTeX plus al-folio extras. Grab entries from Google Scholar (quotation-mark icon → BibTeX):

```bibtex
@article{lovelace2026solver,
  title    = {A Fast Solver for Something},
  author   = {Lovelace, Ada and Babbage, Charles},
  journal  = {Journal of Results},
  year     = {2026},
  selected = {true},
  abbr     = {JoR},
  pdf      = {solver.pdf},
  preview  = {solver.png},
  arxiv    = {2601.01234},
  code     = {https://github.com/adalovelace/solver},
  abstract = {We show that ...},
  bibtex_show = {true}
}
```

| Field | Effect |
|---|---|
| `selected={true}` | Also appears on the about page |
| `abbr` | Venue badge on the left |
| `pdf`, `poster`, `slides`, `supp` | Buttons; bare filenames resolve to `assets/pdf/` |
| `preview` | Thumbnail; file goes in `assets/img/publication_preview/` |
| `arxiv`, `doi`, `hal` | Identifier only — the link is generated |
| `code`, `website`, `blog`, `video` | Full URLs |
| `abstract` | "Abs" expand button |
| `bibtex_show={true}` | "Bib" button showing the raw entry |

Co-author links come from `_data/coauthors.yml`, keyed by lowercase unaccented surname.

#### `_news/`

Two flavours. Inline (renders directly on the about page):

```yaml
---
layout: post
date: 2026-08-11 12:00:00-0400
inline: true
related_posts: false
---

Paper accepted at **NeurIPS 2026**.
```

Linked (gets its own page — add a `title` and drop `inline`). Sorted by `date`, newest first. Filenames are arbitrary; `announcement_1.md` is the template's convention.

#### `_projects/`

```yaml
---
layout: page
title: project name
description: one-line subtitle on the card
img: assets/img/12.jpg
importance: 1               # sort order, 1 = first
category: work              # groups cards when enable_project_categories: true
related_publications: true  # link matching papers.bib entries
---
```

#### `_posts/`

Filename **must** be `YYYY-MM-DD-title.md` or Jekyll silently ignores it.

```yaml
---
layout: post
title: A post about something
date: 2026-08-11 09:00:00
description: shown in listings
tags: numerics julia
categories: research
featured: true              # pins to the top of the blog page
toc:
  sidebar: left             # floating table of contents
---
```

`tags` and `categories` are space-separated (not comma), and drive the related-posts feature.

#### CV (optional)

Two supported formats: `_data/cv.yml` (RenderCV — can auto-generate a PDF via Actions) or `assets/json/resume.json` (JSONResume). Pick one in `_pages/cv.md`:

```yaml
---
layout: cv
cv_format: rendercv         # rendercv | jsonresume
---
```

---

## Part 2 — Local Preview with Docker

Lets you see changes instantly instead of pushing and waiting 5 minutes for CI.

### 1. Start the container

From the repo root:

```bash
docker compose pull
docker compose up
```

First run pulls a ~400 MB image. Subsequent runs are fast.

### 2. Open the site

<http://localhost:8080>

Port is **8080**, not Jekyll's usual 4000.

If you set a `baseurl` (project site), the local URL is `http://localhost:8080/<baseurl>/`.

### 3. Edit and watch

Save any file in the repo — the site rebuilds and the browser reflects it within a few seconds. `_config.yml` is the exception: changes to it require a restart.

### 4. Stop

`Ctrl+C`, then:

```bash
docker compose down
```

### 5. Ship it

```bash
git add .
git commit -m "Update site"
git push
```

Then confirm the green check in the **Actions** tab.

---

## Troubleshooting

**Container starts but the page won't load** — check the build log:

```bash
docker compose up -d
docker compose logs -f
```

**Dependency or gem errors** — go inside and reinstall:

```bash
docker compose exec -it jekyll /bin/bash
bundle install
./bin/entry_point.sh
```

**Stale image after changing `Gemfile`** — rebuild:

```bash
docker compose up --build
```

**Site deploys but CSS is broken / links 404** — `url` or `baseurl` is wrong in `_config.yml`. This is the single most common issue.

**Windows** — run everything inside WSL2. Native Docker Desktop on Windows has known issues with this template.

---

## Notes

- In v1.x, al-folio is a thin starter: layouts, styles, and runtime features live in separate `al_*` Ruby gems declared in the `Gemfile`. Customize via `_config.yml`, content files, and local overrides — don't copy gem-owned files into the repo.
- Upstream docs: [Quick Start](https://github.com/alshedivat/al-folio/blob/main/docs/QUICKSTART.md) · [Install](https://github.com/alshedivat/al-folio/blob/main/docs/INSTALL.md) · [Customize](https://github.com/alshedivat/al-folio/blob/main/docs/CUSTOMIZE.md) · [Troubleshooting](https://github.com/alshedivat/al-folio/blob/main/docs/TROUBLESHOOTING.md)
