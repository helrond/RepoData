---
layout: default
---

# Repositories by State

{% assign states = site.pages | where: "layout","repo" | group_by:"state" %}

{% for page in states %}
  <h2>{{page.name}}</h2>
  <div class="twoColumns">
    {% for item in page.items %}
    <a href="/repos/{{item.id}}">{{item.title}}</a>
    {% endfor %}
  </div>
{% endfor %}
