---
layout: page
title: "CANADALEK"
toc: true
author: CANADALEK
show_title: false
---

# CANADALEK
<div id="archives">
  <div class="archive-group">
    {% capture CANADALEK %}{{ category | first }}{% endcapture %}
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>

    <h4 class="category-head">{{ category_name }}</h4>
    <a name="{{ category_name | slugize }}"></a>
    {% for post in site.categories[category_name] %}
    <article class="archive-item">
      <h4>{{post.date | date: "%-d %B %Y" }} - <a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h4>
    </article>
    {% endfor %}
  </div>
</div>
