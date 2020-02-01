---
layout: article
aside: 
    toc: true
---
<html>
<head></head>
<body>
<center><i>{{page.description}}</i></center>
<hr>    
{% if page.content %}
{{ content }}
{% endif %}

<h3>Related Posts</h3>
  <ul>
    {% for post in site.posts %}
      {% if post.tags contains page.tag %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
      {% endif %}
    {% endfor %}
  </ul>
</body>
</html>
