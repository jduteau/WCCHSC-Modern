# WCCHSC website

Website for the Western Canadian Catholic Home School Conference (www.wcchsc.net / www.wcchsc.org).
Built with Jekyll + Bootstrap 5 (Minty theme) and published with GitHub Pages.

**To update the site for a new year, see [EDITING.md](EDITING.md).** No coding is needed.

## Local preview (optional, for developers)

    bundle install
    bundle exec jekyll serve      # http://localhost:4000

## Layout

| Path | What it is |
|---|---|
| `_data/*.yml` | All the editable content: dates, schedule, speakers, prices, FAQ, colors, menu |
| `*.md` (root) | The pages. Mostly text, with a few `{% include %}` tags |
| `_includes/`, `_layouts/` | HTML building blocks. Normally not edited |
| `_sass/`, `assets/main.scss` | Styling. Colors come from `_data/theme.yml` |
| `assets/img/` | Pictures and the brochure PDF |
| `.github/workflows/pages.yml` | Builds and deploys on every push to `master` |
