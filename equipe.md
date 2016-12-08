---
layout: page
title: Equipe
navigation_weight: 3
---

  {% for member in site.data.members %}
  <h2>{{member.nom}}</h2>
<p>{{member.cursus}}</p><br/>
  {% endfor %}