---
layout: default
permalink: /state/
---

# Repositories by State

{% assign states = site.pages | where: "layout","repo" | group_by:"state" %}

{% for page in states %}
  <h2>{{page.name}}</h2>
  <div class="twoColumns">
    {% for item in page.items %}
    <p><a href="{{site.baseurl}}/repos/{{item.id}}">{{item.title}}</a></p>
    {% endfor %}
  </div>
{% endfor %}
