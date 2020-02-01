---
layout: page
Title: All Posts
articles:
  excerpt_type: html
aside: 
    toc: true
---

## Tags
{% for tag in site.tags %} **[{{ tag[0] }}](/tag/{{ tag[0] }}/)** {% endfor %}

## [Categories](categories/)
{% for category in site.categories %}
### {{ category[0] }}
{% for post in category[1] %}
  - [{{ post.url }}]({{ post.title }})
    {% endfor %}
{% endfor %}



