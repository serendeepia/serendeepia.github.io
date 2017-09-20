Web page with [jekyll](https://jekyllrb.com/)

To test it in localhost (needs ruby):
```sh
bundle update
bundle install
bundle exec jekyll server
```

Web pages are created adding a new markdown file in the root directory. You only have to add header to the file in order to be recognized:

```
---
layout: mylayout
title: Page Title
navigation_weight: 100
---
```