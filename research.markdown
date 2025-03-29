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
  {% if project.resource %}
  <h3><a href="{{ project.resource }}">{{ project.name }}</a></h3>
  {% else %}
  <h3>{{ project.name }}</h3>
  {% endif %}
  <ul class="datalist">{% for user in project.users %}
    {% assign userdata = site.data.users[user] %}
    {% assign member = site.members | where: "user", user | first %}
    <li><a href="{{ member.url }}">{{ userdata.family }}</a></li>
  {% endfor %}</ul>
  <p><i>{{ project.slogan }}</i></p>
  <p>{{ project.content | markdownify }}</p>
{% endfor %}

<h2>Collaborations</h2>

Other endeavours we work with.

{% for collab in site.collabs %}
  {% if collab.resource %}
  <h3><a href="{{ collab.resource }}">{{ collab.name }}</a></h3>
  {% else %}
  <h3>{{ collab.name }}</h3>
  {% endif %}
  <ul class="datalist">{% for user in collab.users %}
    {% assign userdata = site.data.users[user] %}
    {% assign member = site.members | where: "user", user | first %}
    <li><a href="{{ member.url }}">{{ userdata.family }}</a></li>
  {% endfor %}</ul>
  <p><i>{{ collab.slogan }}</i></p>
  <p>{{ collab.content | markdownify }}</p>
{% endfor %}