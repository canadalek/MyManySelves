---
layout: page
Title: Reviews
articles:
  excerpt_type: html
aside: 
    toc: true
---

{% for p in site.posts %}
{% if p.category == "review" %}
  <h3><a href="{{c}}">{{ index.html }}</a></h3>
  <ul>
    {% for post in category %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endif %}
{% endfor %}
