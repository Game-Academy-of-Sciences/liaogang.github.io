---
layout: layout_default  
title: Print All
permalink: /all/
---

<div >
  <hr></hr>
  <ul >{% for post in site.posts %}{% if post.tag != 'private'%}
    <h1>
      <li> <span >{{ post.date | date: "%Y-%m-%d" }} </span> <a {% if post.tag == 'picture' %}href="{{ post.url | prepend: site.baseurl }}"{% endif %}>{{ post.title }}</a> </li> 
    </h1>{% if post.tag != 'picture' %}<div class="content">{{ post.content }}{% endif %}
    </div>
  <hr></hr>{% endif %}{% endfor %}
  </ul>
</div>