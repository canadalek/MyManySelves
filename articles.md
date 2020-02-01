---
layout: page
Title: All Pages
articles:
  excerpt_type: html
aside: 
    toc: true
---
## Pages
<ul>
{% for p in site.pages %}
<li><a href="{{ p.url }}">{{ p.url }}</a> <b>[{{ p.tags }}]</b></li>
    {% if p.keywords %}
    <br>keywords:
    <ul>
        {% for k in p.keywords %}
            <li>{{ k }}</li> 
        {% endfor %}
    </ul>
    {% endif %}
{% endfor %}
</ul>



## [Collections](Collections)
{% for c in site.collections %}
### {{c.label}}
<ul>
{% for p in c.docs %}
    <li><a href="{{ p.url }}">{{ p.url }}</a> <b>({{ p.key }})</b></li>
    {% if c.label == "bibdetails" %}
    <br>keywords:
    <ul>
        {% for k in p.keywords %}
            <li>{{ k }}</li> 
        {% endfor %}
    </ul>
    {% endif %}
{% endfor %}
</ul>
{% endfor %}


## category
{% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% for post in category[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}


## Tags
{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

