# create github.io pages

Edit your `README.md` file. 

- When using links, use markdown syntax `[text](file.md)`.
- `.md` pages are automatically converted to `html` with the configuration below

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

## Jekyll Theme Primer

- Github page: [https://github.com/pages-themes/primer](https://github.com/pages-themes/primer)
- Preview: [https://pages-themes.github.io/primer/](https://pages-themes.github.io/primer/)

Change Layout

~~~
test -d _layouts || mkdir _layouts
cd _layouts
wget https://raw.githubusercontent.com/pages-themes/primer/master/_layouts/default.html
vi default.html
cd ..
git add _layouts/default.html
git commit -m "got layout file 'default.html' from https://pages-themes.github.io/primer/" _layouts/default.html
~~~
