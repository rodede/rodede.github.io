---
layout: page
title: rodede blog
tagline: blog
description: thoughts
---
<div id="content">
{% assign posts_collate = site.posts %}
{% include JB/posts_collate %}



{% for category in site.categories %}
  <div class="content">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>

    <h3 class="category-head">{{ category_name }}</h3>
    <a name="{{ category_name | slugize }}"></a>
    {% for post in site.categories[category_name] %}
    <article class="archive-item">
      <h4><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h4>
    </article>
    {% endfor %}
  </div>
{% endfor %}

</div>


[Markdown](https://daringfireball.net/projects/markdown/) 

[Jekyll](https://jekyllrb.com/)

[Overview](pages/overview.html)  

