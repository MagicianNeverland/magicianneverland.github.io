---
layout: post
title: "blog theme modified log"
description: "record for plan"
categories: [Tech]
tags: [blog, jekyll]
redirect_from:
  - /2018/05/15/
---
# 2018.08.15 update

Finished:

Fixed Menu bug, added 'neverland' button in `_includes/blog/overlay.html`

To Do:

The font of [CJK Unified Ideographs](https://en.wikipedia.org/wiki/CJK_Unified_Ideographs) in this blog is default now. I try to find some open source fonts to make them more beautiful.

3 steps to solve this problem:

1.Choose a font. Now I find [Source Han Serif](https://github.com/adobe-fonts/source-han-serif)

ttf version [here](https://github.com/Pal3love/Source-Han-TrueType)

Some other choices: [Open Source Fonts Collection for Chinese](https://github.com/DrXie/OSFCC)

2.Change the css file, choose right font depending on language.

[the answer from stackoverflow](https://stackoverflow.com/questions/535616/can-css-choose-a-different-default-font-and-size-depending-on-language)

the point is to use the attribute `unicode-range` in `@font-face`

3.Try to find tool to compress the font file load in blog.

someone wrote about this problem in [blog](https://leonax.net/p/7750/use-noto-sans-cjk-as-default-blog-font/) and mentioned TypeKit. But considering about the risk of block by G/F/W, I give it up.

Then I find [Smart webfont compression and format conversion tool](https://github.com/allanguys/font-spider-plus)

I will try these 3 steps above next time.


# 2018.07.26 update

Finished：

1.Added `_includes/helpers/categories_list_sp.html` for specical categories page, filtered the neverland part. Because of this change, modified `blog/categories/index.html`

2.Modified `_includes/helpers/posts_collate.html` and filter the neverland part.

3.Added `blog/neverland`

To Do:

1.Subtags didn't work

2.readme.md


# 2018.05.15 update

Finished：

1.Home page 2 -> 3

2.Modified`_config.yml`for personal settings

3.Modified copyright

To Do:

1.In Home page section1, class "text-box" need to adapt for phone client

`_layouts/home.html`, `_sass/simple-texture-home.scss`

2.disqus still has bugs