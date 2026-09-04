# cdfferguson.github.io

Personal site — blog, CV and about page — built with [Jekyll][] and published
by [GitHub Pages][] at <https://cdfferguson.github.io>.

## Editing the site

Nearly everything lives in one of four places:

| What you want to change | File to edit |
| --- | --- |
| Site title, description, social links | `_config.yml` |
| The homepage introduction | `index.html` |
| The about page | `about.md` |
| The CV | `_data/cv.yml` |

Colours, spacing and fonts are all custom properties at the top of
`assets/css/style.css`.

## Writing a blog post

Create a file in `_posts/` named `YYYY-MM-DD-some-slug.md`:

```markdown
---
title: "Post title"
subtitle: "An optional one-liner shown under the title."
date: 2026-09-04 09:00:00 +0000
tags: [notes]
---

The body of the post, in Markdown.
```

Commit and push it. GitHub Pages rebuilds and publishes within a minute or so.

Drafts go in a `_drafts/` directory without a date in the filename; they are
not published until moved into `_posts/`.

## Previewing locally (optional)

Requires Ruby.

```sh
bundle install
bundle exec jekyll serve --livereload
```

The site is then at <http://localhost:4000> and rebuilds as you save.

## Structure

```
_config.yml        site settings
_data/cv.yml       CV content, rendered by the cv layout
_includes/         head, nav and footer fragments
_layouts/          default, page, post and cv templates
_posts/            blog posts, one Markdown file each
assets/css/        the stylesheet
index.html         homepage
about.md  cv.md  blog.html  404.html
```

[Jekyll]: https://jekyllrb.com
[GitHub Pages]: https://pages.github.com

## Using a custom domain

GitHub Pages serves this at `cdfferguson.github.io` by default. To use your own
domain instead:

1. Add a `CNAME` file at the repository root containing just the domain,
   e.g. `chris.cferguson.org`.
2. At your DNS provider, point that name at GitHub:
   - a subdomain (`www` or `chris`) → a `CNAME` record to `cdfferguson.github.io`
   - an apex domain (`cferguson.org`) → `A` records to `185.199.108.153`,
     `185.199.109.153`, `185.199.110.153` and `185.199.111.153`
3. Update `url:` in `_config.yml` to match, so canonical links and the RSS feed
   point at the right place.
4. In the repository's **Settings → Pages**, enter the domain and tick
   *Enforce HTTPS* once the certificate has been issued.
