---
layout: default
title: Home
lang: en
---

<h1>Welcome to Loopi</h1>
<p class="lead">Unlocking logic and coding for kids, through play—with or without a screen.</p>

<div class="lang-switch">
  <a href="{{ site.baseurl }}/fr/">Voir en Français</a>
</div>

<div class="category-section">
  <h2>Categories</h2>

  {% assign categories = "Débranché (sans ordinateur),Numérique (avec écran),Jeux de société,Dictionnaire (écosystème)" | split: "," %}

  {% for cat in categories %}
    <section>
      <h3>{{ cat }}</h3>
      <div class="resources-grid">
        {% assign resources = site.html_pages | where: "lang", "en" | where: "category", cat %}
        {% for resource in resources %}
          <div class="resource-card">
            <h4><a href="{{ resource.url | relative_url }}">{{ resource.title }}</a></h4>
            <p><small class="status-tag">{{ resource.status }}</small></p>
          </div>
        {% endfor %}
      </div>
    </section>
  {% endfor %}
</div>
