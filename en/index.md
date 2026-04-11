---
layout: default
title: Home
lang: en
---

<h1>Welcome to Loopi</h1>
<p>Unlocking logic and coding for kids, through play—with or without a screen.</p>

<div class="lang-switch">
  <a href="{{ site.baseurl }}/fr/">Voir en Français</a>
</div>

<p>🌐 Online website: <a href="https://seiza.github.io/loopi">https://seiza.github.io/loopi</a></p>

<h2>Categories</h2>

{% assign categories = "Débranché (sans ordinateur),Numérique (avec écran),Jeux de société,Dictionnaire (écosystème)" | split: "," %}

{% for cat in categories %}
  <h3>{{ cat }}</h3>
  <ul>
    {% assign resources = site.html_pages | where: "lang", "en" | where: "category", cat %}
    {% for resource in resources %}
      <li><a href="{{ resource.url | relative_url }}">{{ resource.title }}</a> - <small>{{ resource.status }}</small></li>
    {% endfor %}
  </ul>
{% endfor %}
