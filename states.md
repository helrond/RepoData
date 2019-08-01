---
layout: default
---

# Repositories by State

{% assign states = site.pages | where: "layout","repo" | group_by:"state" %}

{% for page in states %}
  <h1>{{page.name}}</h1>
  <ul>
    {% for item in page.items %}
    <li><a href="/repos/{{item.id}}">{{item.title}}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
