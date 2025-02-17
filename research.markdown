---
title: Research
layout: page
---

<h2>Themes</h2>

Vectors around which our research is oriented.

{% for theme in site.themes %}
  <h3>{{ theme.name }}</h3>
  <p><i>{{ theme.slogan }}</i></p>
  <p>{{ theme.content | markdownify }}</p>
{% endfor %}

<h2>Projects</h2>

Projects that our members are involved in.

{% for project in site.projects %}
  <h3>{{ project.name }}</h3>
  <p><i>{{ project.slogan }}</i></p>
  <ul>{% for user in project.users %}
    {% assign member = site.data.users[user] %}
    <li>{{ member.family }}</li>
  {% endfor %}</ul>
  <p>{{ project.content | markdownify }}</p>
{% endfor %}