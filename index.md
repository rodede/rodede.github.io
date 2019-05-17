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

    <h4 class="category-head">{{ category_name }}</h4>
    <a name="{{ category_name | slugize }}"></a>
    {% for post in site.categories[category_name] %}
    <article class="archive-item">
      <h6><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h6>
    </article>
    {% endfor %}
  </div>
{% endfor %}
        </td>
    </tr>
</table>

<h2 class="category-head">Pages</h2>
- title: Links
  url: pages/links.html

</div>


[Markdown](https://daringfireball.net/projects/markdown/) 

[Jekyll](https://jekyllrb.com/)

[Overview](pages/overview.html)  

