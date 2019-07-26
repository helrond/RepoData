---
layout: default
---

# Repositories

[View all](all/) (beware this is a very long list)

{% assign states = site.pages | where: "layout","repo" | group_by:"state" %}

{% for page in states %}
  <h1>{{page.name}}</h1>
  <ul>
    {% for item in page.items %}
    <li>{{item.title}}</li>
    {% endfor %}
  </ul>
{% endfor %}
