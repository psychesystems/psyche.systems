---
title: Members
layout: page
---


{% assign usernames_array = site.data.groups["staff"] | concat: site.data.groups["students"] %}

{% for username in usernames_array %}
  {% assign user = site.data.users[username] %}
  {% if user %}
  {% assign member = site.members | where: "user", username | first %}
  <div>
  <h2 class="membername">
  {% if member %}
  <a href="{{ member.url }}">{{ user.name }}</a>
  {% else %}
  <span>{{ user.name }}</span>
  {% endif %}
  </h2>
  <p class="memberrole">{{ user.position }}</p>
  </div>
  {% endif %}
{% endfor %}

<h2>Alums</h2>

{% assign usernames_array = site.data.groups["alums"] %}

{% for username in usernames_array %}
  {% assign user = site.data.users[username] %}
  {% if user %}
  {% assign member = site.members | where: "user", username | first %}
  <div>
  <h2 class="membername">
  {% if member %}
  <a href="{{ member.url }}">{{ user.name }}</a>
  {% else %}
  <span>{{ user.name }}</span>
  {% endif %}
  </h2>
  <p class="memberrole">{{ user.position }}</p>
  </div>
  {% endif %}
{% endfor %}

