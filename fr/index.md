---
layout: default
title: Accueil
lang: fr
---

<h1>Bienvenue sur Loopi</h1>
<p>Démystifier la logique et le code pour les enfants par le jeu—avec ou sans écran.</p>

<div class="lang-switch">
  <a href="{{ site.baseurl }}/en/">View in English</a>
</div>

<p>🌐 Site en ligne : <a href="https://seiza.github.io/loopi">https://seiza.github.io/loopi</a></p>

<h2>Catégories</h2>

{% assign categories = "Débranché (sans ordinateur),Numérique (avec écran),Jeux de société,Dictionnaire (écosystème)" | split: "," %}

{% for cat in categories %}
  <h3>{{ cat }}</h3>
  <ul>
    {% assign resources = site.html_pages | where: "lang", "fr" | where: "category", cat %}
    {% for resource in resources %}
      <li><a href="{{ resource.url | relative_url }}">{{ resource.title }}</a> - <small>{{ resource.status }}</small></li>
    {% endfor %}
  </ul>
{% endfor %}
