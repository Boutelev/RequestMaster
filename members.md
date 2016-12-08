---
layout: members
title: Membres
---

  <main>
  {% for member in site.members %}
  <h2>{{members.nom}}</h2>
  <img src="members.avatar" alt="members.nom"/>
<p>{{member.hobbies}}</p><br/>
<p>{{member.cursus}}</p><br/>
<p>{{member.motivation}}</p><br/>
<p>{{member.amis}}</p><br/>


  {% endfor %}
  </main>
