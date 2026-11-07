# antonbanta.github.io

Source for Anton Banta's personal website, <https://antonbanta.github.io>. Built with Jekyll on the
[academic-homepage](https://github.com/luost26/academic-homepage) template and served by GitHub Pages
(every push to `main` redeploys the site).

## Where things live

| What | File |
| --- | --- |
| Name, bio, positions, links, meeting link, education, experience, awards | `_data/profile.yml` |
| Research page sections (and the homepage "Research areas" tiles) | `_data/research.yml` |
| Publications (one file each) | `_publications/<year>/*.md` |
| Patents | `_data/patents.yml` |
| Names to bold or link in author lists | `_data/authors.yml` |
| Navbar tabs | `_data/navigation.yml` |
| Homepage sections on/off | `_data/display.yml` |

## Adding a publication

Create `_publications/<year>/<short-name>.md`:

```yaml
---
title:    "Paper title"
date:     2026-01-31 00:00:00 -0800   # used for sorting
selected: true                        # show on the homepage
pub:      "Journal or venue"
pub_post: ", 12, 3456,"               # optional volume/pages, shown after the venue
pub_date: "2026"
abstract: >-
  One or two sentences on what the paper shows.
authors:
  - "A. Banta"
  - "Co-author name"
topics: [csf]                         # csf, bci, cardiac: lists the paper on the matching research section
links:
  Paper: https://doi.org/...
---
```

## Running locally

```bash
bundle install
bundle exec jekyll serve   # then open http://localhost:4000
```
