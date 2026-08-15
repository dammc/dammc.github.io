# Crosscurrents blog template

A lightweight personal blog for essays at the intersection of sociology, economics, software development, and data science. It uses Jekyll as supported by GitHub Pages, handwritten layouts, plain CSS, system fonts, and no client-side JavaScript.

## Local development

The project targets Ruby 3.3.4. Install Ruby and Bundler, then run:

```bash
bundle install
bundle exec jekyll doctor
bundle exec jekyll build --trace
bundle exec jekyll serve
```

Open `http://localhost:4000`. To make a production-style build without starting a server:

```bash
JEKYLL_ENV=production bundle exec jekyll build --trace
```

Generated output is written to `_site/` and should not be edited or committed.

## Customize the site

Edit `_config.yml` to set the site title, description, public URL, author name, and contact email. If the repository is published as a project site rather than `username.github.io`, set `baseurl` to the repository name, for example `/my-blog`.

Replace `assets/images/profile-placeholder.svg` with your portrait and update the image path, dimensions, and alternative text in `index.html`. Replace the marked placeholder About text there as well. The homepage automatically lists published posts in reverse chronological order.

## Write a post

Add Markdown files to `_posts/` using the `YYYY-MM-DD-short-title.md` filename format:

```yaml
---
title: A descriptive article title
description: A short summary used on the homepage and in page metadata.
---
```

Posts receive the article layout automatically and are published at `/blog/short-title/`.

The post layout renders the title from front matter as the article's sole `<h1>`. Do not add a `#` heading in the Markdown body. Begin top-level article sections at `##`, use `###` for their subsections, and continue nesting without skipping heading levels.

For an image and caption, store an optimized local image under `assets/images/posts/` and use the figure include. The `src`, meaningful `alt`, and positive intrinsic `width` and `height` parameters are required; `caption` is optional and accepts plain text. Do not pass empty alternative text through this article-figure include. If an article genuinely needs a decorative image, use separate explicit markup so that decision is visible during review. Liquid cannot determine whether alternative text is meaningful, so inspect the built HTML before publishing.

```liquid
{% include figure.html
  src="/assets/images/posts/example/chart.svg"
  alt="A line chart showing the described trend"
  width="960"
  height="540"
  caption="Figure 1. A concise explanation and source."
%}
```

Kramdown renders footnote references as linked superscript numbers and adds backlinks from the notes at the end of the article:

```markdown
A claim with a remark.[^remark]

A sourced claim.[^source]

## Notes
{: .footnotes-heading}

[^remark]: A short explanatory note.
[^source]: [Source title](https://example.com/).
```

Keep the `## Notes` heading, its `{: .footnotes-heading}` class line, and all footnote definitions as the final content in the article. This gives the generated endnotes a semantic heading while preserving Kramdown's linked references and backlinks.

`_posts/2026-08-14-rendering-fixture.md` is intentionally non-substantive. It exists to verify figures, captions, code, tables, footnotes, and the homepage listing; replace or remove it when publishing real work.

## Structure

| Path | Responsibility |
| --- | --- |
| `_config.yml` | Site metadata, routes, and Markdown settings |
| `_layouts/` | Shared page shell and article layout |
| `_includes/figure.html` | Accessible captioned figures |
| `_posts/` | Markdown articles |
| `index.html` | Blog, About, and Contact sections |
| `assets/css/main.css` | Responsive typography-led design |
| `assets/images/` | Local portraits and article media |

## Publish with GitHub Pages

Push the repository to GitHub, then in **Settings → Pages** select **Deploy from a branch**, choose the publishing branch, and use the repository root. GitHub Pages will run its supported Jekyll build. No custom deployment workflow is required.

## Codex development environment

Repository-wide constraints are in `AGENTS.md`; the repeatable platform workflow is in `.agents/skills/blog-development/SKILL.md`; specialized agent definitions and conservative command rules live under `.codex/`. These files support development and are excluded from the generated site where applicable.
