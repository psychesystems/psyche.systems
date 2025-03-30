---
title: Members
layout: page
---

{% comment %} retrieve all users and sort them by role {% endcomment %}
{% assign investigators_array = "" | split: "" %}
{% assign researchers_array = "" | split: "" %}
{% assign students_array = "" | split: "" %}
{% for userdata in site.data.users %}
  {% assign username = userdata[0] %}
  {% assign user = userdata[1] %}
  {% if user.role == "investigator" %}
    {% assign investigators_array = investigators_array | push: username %}
  {% endif %}
  {% if user.role == "researcher" %}
    {% assign researchers_array = researchers_array | push: username %}
  {% endif %}
  {% if user.role == "student" %}
    {% assign students_array = students_array | push: username %}
  {% endif %}
{% endfor %}

{% assign usernames_array = investigators_array | concat: researchers_array | concat: students_array %}

{% for username in usernames_array %}
  {% assign user = site.data.users[username] %}
  {% assign member = site.members | where: "user", username | first %}
  <div>
  <h2 class="membername">
  <a href="{{ member.url }}">{{ user.name }}</a>
  </h2>
  <p class="memberrole">{{ user.position }}</p>
  </div>
{% endfor %}

