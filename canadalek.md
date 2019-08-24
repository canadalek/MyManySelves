---
layout: page
title: ""
toc: true
show_title: false
---

#CANADALEK
<div id="archives">
  <div class="archive-group">
    {% capture CANADALEK %}{{ category | first }}{% endcapture %}
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>

    <h4 class="category-head">{{ category_name }}</h3>
    <a name="{{ category_name | slugize }}"></a>
    {% for post in site.categories[category_name] %}
    <article class="archive-item">
      <h4>{{post.date | date: "%-d %B %Y" }} - <a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h4>
    </article>
    {% endfor %}
  </div>
{% endfor %}
</div>
