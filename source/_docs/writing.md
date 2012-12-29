---
layout: page
title: Writing
date: 2012-11-01 18:13:30
---

## Post

### Create

Execute the following command.

``` bash
hexo new_post <title>
```

New post will saved at `source/_posts/name.md` in the root directory with the following content.

File name is based on `new_post_name` setting in `_config.yml`, and title will be transformed into lower case, spaces will be transformed into dash. For example:

```
hexo new_post Test Post => source/_posts/test-post.md
```

``` yaml
---
layout: post
title: title
date: YYYY-MM-DD HH:mm:ss
comments: true
tags:
---
```

### Configure

The beginning of article is a block wrapped with `---`, called [YAML Front Matter]. You can use YAML to configure posts.

The following is default configuration. You can modify them as you like.

- **layout** - Article layout
- **title** - Article title
- **date** - Published date of article (Format is `YYYY-MM-DD HH:mm:ss`)
- **comments** - Enable comment for this article
- **tags** - Tags of article
- **permalink** - Override default URL (Optional)

### Category

Category is the relative path to `source/_posts`. It's hierarchical.

For example:

- `source/_posts/title.md` - Uncategorized
- `source/_posts/Fruits/title.md` - Fruit
- `source/_posts/Fruits/Apple/title.md` - Fruit, Apple

### Tag

``` yaml
# Single Tag
tags: Apple

# Multiple Tags
tags: [Apple, Banana]

tags:
- Apple
- Banana
```

## Page

### Create

Execute the following command.

``` bash
hexo new_page <title>
```

New page will saved at `source/name/index.md` in the root directory with the following content.

Title will be transformed into lower case, spaces will be transformed into dash. For example:

```
hexo new_page Test Page => source/test-page/index.md
```

``` plain
---
layout: page
title: title
date: YYYY-MM-DD HH:mm:ss
comments: true
---
```

### Configure

The beginning of article is a block wrapped with `---`, called [YAML Front Matter]. You can use YAML to configure posts.

The following is default configuration. You can modify them as you like.

- **layout** - Article layout
- **title** - Article title
- **date** - Published date of article (Format is `YYYY-MM-DD HH:mm:ss`)
- **comments** - Enable comment for this article
- **permalink** - Override default URL (Optional)

## Generate Static Files

Execute the following command to transform articles into static files.

``` bash
hexo generate
```

[YAML Front Matter]: https://github.com/mojombo/jekyll/wiki/YAML-Front-Matter