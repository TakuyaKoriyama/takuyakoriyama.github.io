# Takuya Koriyama — personal website

Research in statistics, machine learning, and probability.

Public website: https://takuyakoriyama.github.io/

## Editing

| Content | File |
| --- | --- |
| Papers | `_data/researcher.json` |
| Introduction and research interests | `_layouts/researcher.html` |
| Education and experience | `_includes/researcher/cv.html` |
| Profile links and analytics | `_config.yml` |
| Research blog | `_research_blog/*.md` |
| CV source and PDF | `cv.tex`, `out/cv.pdf` |
| Styles | `assets/css/researcher.css` |
| Portrait | `images/profile_new.jpg` |

See `_docs/MAINTENANCE.txt` and `_docs/BLOGGING.txt` for details.

## Preview

```sh
bundle install
bundle exec jekyll serve --config _config.yml,_config.dev.yml
```

Validate the production build with:

```sh
JEKYLL_ENV=production bundle exec jekyll build --safe
```

GitHub Pages publishes the root of `master`. Pushing changes to `master`
automatically updates the public website.

## Attribution

Originally based on [AcademicPages](https://academicpages.github.io/) and
[Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/). Legacy theme
files and example content have been removed. See `LICENSE` for attribution.
