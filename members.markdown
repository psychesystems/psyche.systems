---
title: Members
layout: page
---


{% assign usernames_array = site.data.groups["investigator"] | concat: site.data.groups["researcher"] | concat: site.data.groups["student"] %}

{% for username in usernames_array %}
  {% assign user = site.data.users[username] %}
  {% if user %}
  {% assign member = site.members | where: "user", username | first %}
  <div>
  <h2 class="membername">
  <a href="{{ member.url }}">{{ user.name }}</a>
  </h2>
  <p class="memberrole">{{ user.position }}</p>
  </div>
  {% endif %}
{% endfor %}

