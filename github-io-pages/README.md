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
theme: jekyll-theme-tactile
~~~

- [GitHub Docs: Setting up a GitHub Pages site with Jekyll](https://docs.github.com/en/github/working-with-github-pages/setting-up-a-github-pages-site-with-jekyll)
