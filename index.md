---
layout: page
title: rodede blog
tagline: blog
description: thoughts
---
<div id="content">
<table>
    <tr>
        <td>
           {% assign posts_collate = site.posts %}
           {% include JB/posts_collate %}
        </td>
        <td>        
{% for category in site.categories %}
  <div class="content">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>

    <h4 class="category-head">{{ category_name }}</h3>
    <a name="{{ category_name | slugize }}"></a>
    {% for post in site.categories[category_name] %}
    <article class="archive-item">
      <h6><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h4>
    </article>
    {% endfor %}
  </div>
        </td>
    </tr>
</table>


</div>


[Markdown](https://daringfireball.net/projects/markdown/) 

[Jekyll](https://jekyllrb.com/)

[Overview](pages/overview.html)  

