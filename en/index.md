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

<section>
  <h3>The 3 golden rules for parents</h3>
  <ol>
    <li><b>The right to make mistakes</b>: In coding, we don't make mistakes, we "bug". It's a great opportunity to look for the solution together ("debugging").</li>
    <li><b>The creative aspect</b>: Don't ask them to "code for the sake of coding". Ask them: "What story or game would you like to invent?"</li>
    <li><b>Encourage collaboration</b>: With twins, it's tempting to compare. Instead, encourage them to do "Pair Programming": one types/manipulates, the other checks the logic, then swap roles every 15 minutes.</li>
  </ol>
</section>

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
