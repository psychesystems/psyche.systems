---
title: Members
layout: page
---

{% for member in site.members %}
  {% assign user = site.data.users[member.user] %}
  <div>
    <h2 class="membername">
      <a href="{{ member.url }}">{{ user.name }}</a>
    </h2>
    <p class="memberrole">{{ user.title }}</p>
  </div>
{% endfor %}