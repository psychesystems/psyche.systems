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
  <p><i>{{ project.slogan }}</i></p>
  <ul class="projectmember">{% for user in project.users %}
    {% assign member = site.data.users[user] %}
    <li class="projectmember">{{ member.family }}</li>
  {% endfor %}</ul>
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
  <p><i>{{ collab.slogan }}</i></p>
  <ul class="projectmember">{% for user in collab.users %}
    {% assign member = site.data.users[user] %}
    <li class="projectmember">{{ member.family }}</li>
  {% endfor %}</ul>
  <p>{{ collab.content | markdownify }}</p>
{% endfor %}