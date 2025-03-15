---
layout: default
---

# Posts

{% for post in site.posts %}
  <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>  
  <p>{{post.description}}</P>
{% endfor %}