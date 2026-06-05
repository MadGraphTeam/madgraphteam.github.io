# madgraphteam.github.io
MadGraph website — source for [madgraph.org](https://madgraph.org), built with [Jekyll](https://jekyllrb.com) and hosted on GitHub Pages.

## Local development

**Prerequisites:** Ruby ≥ 3.0 and Bundler (`gem install bundler`).

1. Install dependencies:
   ```bash
   bundle install
   ```

2. Start the local server with live reload:
   ```bash
   bundle exec jekyll serve --livereload
   ```

3. Open [http://localhost:4000](http://localhost:4000) in your browser. The site rebuilds automatically whenever you save a file.

To do a one-off build without serving (output goes to `_site/`):
```bash
bundle exec jekyll build
```

## Content editing

| What to change | File |
|---|---|
| Site title, URLs, external links | `_config.yml` |
| Landing page | `index.html` |
| Team members and institutions | `_data/team.yml` |
| Publications list | `_data/publications.yml` |
| Styles | `_sass/main.scss` |
| Navigation / footer | `_includes/header.html`, `_includes/footer.html` |

Team member photos go in `assets/images/team/` and are referenced in `_data/team.yml` via the `photo:` field (e.g. `photo: /assets/images/team/jane-doe.jpg`).

The logo placeholder in the header is a dashed square in `_includes/header.html` — replace the `<div class="logo-placeholder">` element with an `<img>` tag once the logo is ready.
