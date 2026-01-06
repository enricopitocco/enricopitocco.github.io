# Copilot Instructions for Academic Pages Portfolio

This repository is a personal academic portfolio website based on the Academic Pages template, using Jekyll and GitHub Pages.

## Project Overview

This is a Jekyll-based static site for an academic portfolio, including publications, talks, teaching materials, and CV information.

## Technology Stack

- **Static Site Generator**: Jekyll (Ruby-based)
- **Hosting**: GitHub Pages
- **Theme**: Academic Pages (forked from Minimal Mistakes)
- **JavaScript Dependencies**: jQuery, FitVids, Plotly.js
- **Package Management**: Bundler (Ruby), npm (JavaScript)

## Build and Development

### Local Development

To run the site locally:

```bash
bundle install
jekyll serve -l -H localhost
```

Or with bundle exec:

```bash
bundle exec jekyll serve -l -H localhost
```

### Using Docker

The repository includes Docker support. To run with Docker:

```bash
chmod -R 777 .
docker compose up
```

The site will be available at `localhost:4000`.

### JavaScript Build

To build minified JavaScript:

```bash
npm run build:js
```

## File Structure and Conventions

- **Configuration**: `_config.yml` contains site-wide settings
- **Content**:
  - `_pages/`: Main pages (About, CV, etc.)
  - `_posts/`: Blog posts in Markdown
  - `_publications/`: Publication entries
  - `_talks/`: Talk entries
  - `_teaching/`: Teaching materials
  - `_portfolio/`: Portfolio items
- **Layout**: `_layouts/` contains page templates
- **Includes**: `_includes/` contains reusable components
- **Styles**: `_sass/` contains SCSS stylesheets
- **Static Assets**: 
  - `assets/`: JavaScript, CSS, images
  - `files/`: PDFs and downloadable files
  - `images/`: Image files

## Important Guidelines

### Configuration Changes

- Main configuration is in `_config.yml`
- Changes to `_config.yml` require restarting the Jekyll server
- Markdown and HTML changes are hot-reloaded automatically

### Content Guidelines

- Use Markdown for content files
- Follow existing frontmatter structure in similar files
- Keep files organized in their respective directories

### Styling

- Follow the existing SCSS structure in `_sass/`
- The theme supports "default" and "air" options via `site_theme` in `_config.yml`

### Dependencies

- Ruby dependencies are managed in `Gemfile`
- JavaScript dependencies are in `package.json`
- Always run `bundle install` after updating `Gemfile`
- Run `npm install` after updating `package.json`

### Code Style

- Follow Jekyll/Liquid templating conventions for layouts and includes
- Use existing code style from the template
- Maintain consistency with the Academic Pages theme structure

## Testing Changes

Before committing changes:

1. Test locally with `jekyll serve -l -H localhost`
2. Verify all pages render correctly
3. Check that navigation and links work
4. Ensure responsive design works on different screen sizes

## References

- Academic Pages documentation: https://academicpages.github.io/
- Jekyll documentation: https://jekyllrb.com/docs/
- GitHub Pages documentation: https://docs.github.com/en/pages
