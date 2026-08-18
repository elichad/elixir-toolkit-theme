---
title: Blog
description: Latest updates from the ETT community
permalink: /blog
sidebar: blog
---

Create a blog landing page with the following content:

```
---
title: Blog
description: Latest updates from the ETT community
permalink: /blog
sidebar: blog
---

{% raw %}
{% include blog_posts.html %}
{% endraw %}
```

The `blog` sidebar and blog post feed are automatically populated:

{% include blog_posts.html %}

<hr>

## Creating a post

See [Writing a blog post - template]({% link _blog/2026-08-18/writing-blog-posts.md %}).

## Previewing a post

Follow the [local deployment instructions](https://github.com/ELIXIR-Belgium/elixir-toolkit-theme#locally-using-jekyll) to preview a blog post on the website.

By default, posts with a publication date in the future will not be displayed. Use `bundle exec jekyll serve --future` to display future posts.

## Publishing a post

By default, posts with a publication date in the future will not be displayed. This means a post can be merged into the website a few days before its intended publication. However, you do need to ensure that the site is rebuilt on the publication date in order for the post to show up - this can be achieved by [scheduling the GitHub Actions deployment workflow](https://docs.github.com/en/actions/how-tos/write-workflows/choose-when-workflows-run/trigger-a-workflow#schedule) to run on a regular basis.
