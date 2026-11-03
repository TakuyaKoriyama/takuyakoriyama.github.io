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

This Mac uses a dedicated Conda environment with Ruby 3.3. For a fresh setup
(with Conda already installed), run once:

```sh
conda create -n website-preview --override-channels -c conda-forge ruby=3.3 c-compiler cxx-compiler
conda activate website-preview
bundle install
```

For each preview session:

```sh
conda activate website-preview
bundle exec jekyll serve --config _config.yml,_config.dev.yml --livereload
```

Open http://localhost:4000/. Stop the server with Control+C. Restart it after
changing a configuration file. Local previews do not send Google Analytics.
Run `bundle install` again after changing the Gemfile.

This Mac has an environment activation helper that prioritizes the environment's
Ruby and Bundler. To diagnose a command lookup issue, run `command -v ruby bundle`;
both paths should start with the active environment directory. If Bundler resolves
to `/usr/bin/bundle`, correct the current session with:

```sh
export PATH="$CONDA_PREFIX/bin:$CONDA_PREFIX/share/rubygems/bin:$PATH"
rehash
```

See the
[Jekyll macOS guide](https://jekyllrb.com/docs/installation/macos/) for alternative
Ruby setup options.

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
