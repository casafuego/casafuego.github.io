---
layout: default
title: ""
---

Hola, soy Cristhian. Acá escribo de publicidad, ideas y otras cosas que me interesan. 

---

## Temas

<p class="tag-cloud">
{% assign all_tags = site.posts | map: "tags" | join: "," | split: "," | uniq | sort %}
{% for tag in all_tags %}<a href="/temas/{{ tag | slugify }}/">{{ tag }}</a>{% unless forloop.last %}, {% endunless %}{% endfor %}
</p>

---

## Posts

<ul class="post-list">
{% for post in site.posts %}
  <li>
    <span class="post-date">{{ post.date | date: "%Y-%m-%d" }}</span>
    <a href="{{ post.url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
