---
layout: default
permalink: /all/
---

# All Repositories

{% assign alphabet="A,B,C,D,E,F,G,H,I,J,K,L,M,N,O,P,Q,R,S,T,U,V,W,X,Y,Z" | split: "," %}

{% for letter in alphabet %}
  <h2>{{letter}}</h2>
  <ul>
  {% for repo in site.pages %}
    {% assign first = repo.title | slice: 0 %}
    {% if repo.layout == 'repo' and first == letter %}
    <li><a href="/repos/{{repo.id}}">{{repo.title}}</a></li>
    {% endif %}
  {% endfor %}
  </ul>
{% endfor %}
