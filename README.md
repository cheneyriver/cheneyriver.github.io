# Junliang Chen's personal website

Academic profile of Junliang Chen, MPhil student in the AI Thrust at HKUST (Guangzhou).

Website: https://cheneyriver.github.io/

Built with Jekyll and the [Academic Pages](https://github.com/academicpages/academicpages.github.io) template. Original theme attribution is retained in the website footer and LICENSE.

## Update content

| Content | Source |
| --- | --- |
| Name, affiliation, email, GitHub and avatar | `_config.yml` |
| Homepage | `_pages/about.md` |
| Research | `_pages/research.md` |
| Publications (shared across pages) | `_data/publications.yml` |
| Projects (shared across pages) | `_data/projects.yml` |
| CV page | `_pages/cv.md` |
| Downloadable CV | `files/Junliang_CHEN_CV_26_06.pdf` |
| Profile photo | `images/junliang-chen.png` |
| Navigation | `_data/navigation.yml` |
| Personal styling | `assets/css/profile.css` |

Content is based on the supplied June 2026 CV. Publication acceptance statuses are preserved; unavailable publication URLs and academic profile links are omitted. Upstream demonstration pages and collections are excluded in `_config.yml`.

## Deploy

GitHub Pages must use **Settings > Pages > Source: GitHub Actions**. A push to `master` runs the existing **Deploy Academic Pages template site to Pages** workflow, which installs the dependencies in `Gemfile`, builds the site, and deploys it. It can also be run manually from Actions.

## Local development

Install Ruby with its development toolchain (RubyInstaller **with Devkit** on Windows), Bundler, and Node.js. In the repository directory:

```sh
bundle config set --local path vendor/bundle
bundle install
npm install --no-save uglify-js
npx uglifyjs assets/js/plugins/jquery.greedy-navigation.js assets/js/_main.js assets/js/theme.js -c -m -o assets/js/main.min.js
bundle exec jekyll serve --host 127.0.0.1 --port 4000
```

Open http://127.0.0.1:4000/. Restart Jekyll after changing `_config.yml`. Build output, installed dependencies, and local Bundler configuration are ignored by Git.
