---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

# Repositories

<ul>
{% for repo in site.pages %}
  {% if repo.layout == 'repo' %}
  <li><a href="/repos/{{repo.id}}">{{repo.title}}</a></li>
  {% endif %}
{% endfor %}
</ul>
