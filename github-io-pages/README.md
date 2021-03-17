# create github.io pages

Edit your `README.md` file. When using links, use markdown syntax `[text](file.md)`.

Create a `_config.yml` file:

~~~yaml
plugins:
  - jekyll-relative-links
relative_links:
  enabled: true
  collections: true
theme: jekyll-theme-tactile
~~~
