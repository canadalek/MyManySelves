---
layout: home	
author: CANADALEK
show_excerpt: true 
excerpt_type: html
show_tags: true
toc: true
#sidebar: 
#  nav: sidebarlinks	
---

<blockquote>
I contain multitudes. 
Here are their stories. 
None has a legal birth certificate, but they reside in the same meatspace as one who does.
-- Myself
</blockquote>
  
   

Read more:
- [Quark's Musings](quark.html)
- [Canadalek's Musings](canadalek.html)


<h3>Recent Posts:</h3>
<ul>
{% for post in site.posts limit:5 %}
  <li>{{post.date | date: "%-d %B %Y" }} - <a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></li>
{% endfor %}
</ul>


