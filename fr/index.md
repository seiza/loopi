---
layout: default
title: Accueil
lang: fr
---

<h1>Bienvenue sur Loopi</h1>
<p class="lead">Démystifier la logique et le code pour les enfants par le jeu—avec ou sans écran.</p>

<div class="lang-switch">
  <a href="{{ site.baseurl }}/en/">View in English</a>
</div>

  <section>
    <h3>Les 3 règles d'or pour parents</h3>
    <ol>
      <li><b>Le droit à l'erreur</b> : En code, on ne se trompe pas, on "bugue". C’est une opportunité géniale de chercher la solution ensemble (le "debugging").</li>
      <li><b>L'aspect créatif</b> : Ne leur demandez pas de "coder pour coder". Demandez-leur : "Quelle histoire ou quel jeu aimerais-tu inventer ?"</li>
      <li><b>Encouragez la collaboration</b> : Avec des jumeaux, il est tentant de comparer. Incitez-les plutôt à faire du "Pair Programming" : l'un tape/manipule, l'autre vérifie la logique, puis on échange les rôles toutes les 15 minutes.</li>
    </ol>
  </section>

<div class="category-section">
  <h2>Catégories</h2>

  {% assign categories = "Débranché (sans ordinateur),Numérique (avec écran),Jeux de société,Dictionnaire (écosystème)" | split: "," %}

  {% for cat in categories %}
    <section>
      <h3>{{ cat }}</h3>
      <div class="resources-grid">
        {% assign resources = site.html_pages | where: "lang", "fr" | where: "category", cat %}
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
