# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based academic website built on the Academic Pages template. It serves as a personal portfolio for Sasank Desaraju (MD/PhD Candidate at University of Florida), showcasing publications, talks, teaching experience, and blog posts.

The site is hosted on GitHub Pages at: https://sasank-desaraju.github.io

## Technology Stack

- **Static Site Generator**: Jekyll (via github-pages gem)
- **Template**: Academic Pages (forked from Minimal Mistakes Jekyll Theme)
- **Markdown**: Kramdown with GFM input
- **Styling**: Sass/SCSS
- **Plugins**: jekyll-sitemap, jekyll-feed, jekyll-redirect-from, jekyll-paginate, jekyll-gist

## Development Commands

### Local Development

Start the local development server:
```bash
bundle exec jekyll serve
```
Or use the provided script:
```bash
./local_launch.sh
```

The site will be available at `http://localhost:4000`. Jekyll will automatically rebuild on file changes when using the `-l` flag: `bundle exec jekyll serve -l -H localhost`

### Setup

Install dependencies (first time setup):
```bash
bundle install
```

If encountering errors, delete `Gemfile.lock` and run `bundle install` again.

## Site Architecture

### Collections

Jekyll collections define the main content types, configured in `_config.yml`:

- **publications** (`_publications/`): Research papers and academic publications
- **talks** (`_talks/`): Conference presentations and talks
- **teaching** (`_teaching/`): Teaching experience and roles
- **portfolio** (`_portfolio/`): Project portfolio items (currently unused)
- **posts** (`_posts/`): Blog posts

Each collection item is a markdown file with YAML frontmatter defining metadata (title, date, venue, etc.).

### Key Directories

- `_pages/`: Static pages (About, CV, Publications index, etc.)
- `_layouts/`: HTML templates that define page structure
  - `single.html`: Default layout for most content
  - `talk.html`: Specialized layout for talks
  - `archive.html`: List/archive views
- `_includes/`: Reusable HTML components (author profile, navigation, footer, etc.)
- `_sass/`: Sass stylesheets
- `_data/`: YAML data files
  - `navigation.yml`: Defines main site navigation menu
  - `authors.yml`: Author information
  - `ui-text.yml`: UI text strings for internationalization
- `_site/`: Generated static site (excluded from git)
- `files/`: Static files (PDFs, documents) accessible at `/files/`
- `images/`: Image assets
- `assets/`: JavaScript and CSS assets

### Content Structure

**Publications** (`_publications/*.md`):
```yaml
---
title: "Paper Title"
collection: publications
permalink: /publication/short-name
date: YYYY-MM-DD
venue: 'Journal Name'
paperurl: 'https://doi.org/...'
citation: 'Author list'
---
```

**Talks** (`_talks/*.md`):
```yaml
---
title: "Talk Title"
collection: talks
type: "Talk"
permalink: /talks/short-name
venue: "Conference Name"
date: YYYY-MM-DD
location: "City, State"
---
```

**Teaching** (`_teaching/*.md`):
Similar frontmatter structure with role/course information.

### Markdown Generation

The `markdown_generator/` directory contains Jupyter notebooks and Python scripts to bulk-generate markdown files from TSV/BibTeX files:

- `publications.py` / `publications.ipynb`: Generate publication markdown from TSV
- `pubsFromBib.py` / `PubsFromBib.ipynb`: Generate publication markdown from BibTeX
- `talks.py` / `talks.ipynb`: Generate talks markdown from TSV

Use these when adding multiple items at once rather than manually creating individual markdown files.

## Configuration

Site configuration is in `_config.yml`:

- Site metadata (title, description, URL)
- Author/bio information and social media links
- Collection definitions and permalink structures
- Default layouts for each content type
- Plugin configuration
- Sass compilation settings

Navigation menu items are defined in `_data/navigation.yml`.

## Git Workflow

The main branch is `main`. When creating pull requests, use `main` as the base branch.

GitHub Pages automatically builds and deploys on push to `main`.

## Important Notes

- Jekyll uses Liquid templating language in layouts and includes
- Markdown files support both standard markdown and Liquid tags
- The `future: true` setting in config allows posts with future dates to be published
- Static files in `files/` directory are directly accessible at `https://sasank-desaraju.github.io/files/filename.ext`
- The site excludes certain directories from build (node_modules, vendor, etc.) as defined in `_config.yml`
