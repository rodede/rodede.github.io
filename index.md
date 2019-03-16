---
layout: page
title: rodede blog
tagline: blog
description: thoughts
---
<div id="content">
{% assign posts_collate = site.posts %}
{% include JB/posts_collate %}

<ul>
 {% assign categories_list = site.categories %}   
 {% include JB/categories_list %}
</ul>

</div>


[Markdown](https://daringfireball.net/projects/markdown/) 

[Jekyll](https://jekyllrb.com/)

[Overview](pages/overview.html)  

