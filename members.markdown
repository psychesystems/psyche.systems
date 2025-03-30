---
title: Members
layout: page
---

{% for userdata in site.data.users %}
  {% assign username = userdata[0] %}
  {% assign user = userdata[1] %}
  {% assign member = site.members | where: "user", username | first %}
  <div>
    <h2 class="membername">
      <a href="{{ member.url }}">{{ user.name }}</a>
    </h2>
    <p class="memberrole">{{ user.title }}</p>
  </div>
{% endfor %}