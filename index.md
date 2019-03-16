---
layout: page
title: rodede blog
tagline: blog
description: thoughts
---

[Markdown](https://daringfireball.net/projects/markdown/) 

[Jekyll](https://jekyllrb.com/)

[Overview](pages/overview.html)  

    <ul>
          {% assign pages_list = site.pages %}
          {% include JB/pages_list %}
        </ul>


    {% assign posts_collate = site.posts %}
    {% include JB/posts_collate %}
