Web page with [jekyll](https://jekyllrb.com/)

To test it in localhost (needs ruby):
```sh
bundle update
bundle install
bundle exec jekyll server
```

Static web pages are created adding a new markdown or html file in the root directory. You only have to add header to the file in order to be recognized:

```
---
layout: mylayout
title: Page Title
navigation_weight: 100
---
```

Blog post pages are created under `_post` and must start with the date of the post. They also need a header:

```
---
layout: mylayout
title:  "Serendeepia has born"
summary: "This is the summary of the post"
---
```