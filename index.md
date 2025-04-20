---
layout: default
---

# Posts

{% assign all_posts = site.posts | concat: site.data.medium_posts %}
{% assign sorted_posts = all_posts | sort: 'date' | reverse %}

{% for post in sorted_posts %}
  <h2>
    {% if post.url contains "medium.com" %}
      <a href="{{ post.url }}" target="_blank">{{ post.title }}</a>
    {% else %}
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    {% endif %}
  </h2>
  <p>{{ post.description }}</p>
  <p><em>{{ post.date | date: "%B %d, %Y" }}</em></p>
{% endfor %}

# Reading
[Books 2025](/assets/Books2025.html)
