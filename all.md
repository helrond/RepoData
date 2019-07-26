---
layout: default
permalink: /all/
---

# Repositories

<ul>
{% for repo in site.pages %}
  {% if repo.layout == 'repo' %}
  <li><a href="/repos/{{repo.id}}">{{repo.title}}</a></li>
  {% endif %}
{% endfor %}
</ul>
