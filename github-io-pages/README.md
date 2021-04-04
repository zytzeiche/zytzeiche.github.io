# create github.io pages

## github.io main page

- Create a Repository named `<github-username>.github.io`
- Edit your `README.md` file. 
  - When using links, use markdown syntax `[text](file.md)`.
  - `.md` pages are automatically converted to `html` with the configuration below
- The Link to the `github.io` Page will be `https://<github-username>.github.io`
- The Link to the `github.com` Page will be `https://github.com/<github-username>/<github-username>.github.io`

Create a [`_config.yml`](https://github.com/zytzeiche/zytzeiche.github.io/blob/main/_config.yml) file:

~~~yaml
plugins:
  - jekyll-relative-links
relative_links:
  enabled: true
  collections: true
theme: jekyll-theme-primer
~~~

- [GitHub Docs: Setting up a GitHub Pages site with Jekyll](https://docs.github.com/en/github/working-with-github-pages/setting-up-a-github-pages-site-with-jekyll)

## Create a github.io page on another repository

- Choose which directory will hold your published documents

~~~bash
cd "$(git rev-parse --show-toplevel)"
mkdir docs
cd docs
vi docs/index.md
cd ..
git add docs/index.md
git commit -m "initial commit" docs/index.md
git push
~~~

Configuration of the GIT Repo

- Under the repository name, click on `Settings`
- Scroll down to the section `GitHub Pages` and enable GitHub Pages
- The page will be available under `https://<github-username>.github.io/repo`
- The root directory of the subpage (repo) of `<github-username>.github.io`
  will be `./docs`, you cannot reach files outside the `./docs` directory.
- A link to `..` in a file in the `./docs` folder, will _not_ link to the main
  directory in the repo, but will link to the main github.io repository which
  is `<github-username>.github.io`!


## Jekyll Theme Primer

- Github page: [https://github.com/pages-themes/primer](https://github.com/pages-themes/primer)
- Preview: [https://pages-themes.github.io/primer/](https://pages-themes.github.io/primer/)

Change Layout

~~~bash
cd <repo-main-doc-directory>
test -d _layouts || mkdir _layouts
cd _layouts
wget https://raw.githubusercontent.com/pages-themes/primer/master/_layouts/default.html
vi default.html
cd ..
git add _layouts/default.html
git commit -m "got layout file 'default.html' from https://pages-themes.github.io/primer/" _layouts/default.html
~~~

default.html

~~~html
This site hosted on <a href="https://github.com/`{{` site.github.repository_nwo }}">GitHub.com</a> 
~~~

