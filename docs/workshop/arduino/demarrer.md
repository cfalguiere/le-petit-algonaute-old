---
layout: workshop
title: Atelier Arduino
date: '2018-06-17 11:30:00 CET'
category: Arduino
tags: ['Arduino', 'Atelier']
published: true
assetsFolder: /le-petit-algonaute/assets/workshop/arduino/images
---

{% include workshop-icons.ext selected="demarrer" workshop="Arduino" %}

---

<!--
### Démarrer l'atelier de programmation

Pour débuter avec le robot vous pouvez commencer par la description des modes et des ateliers sur chacun des modes

- [Les modes préprogrammés](https://www.thymio.org/fr:thymiostarting)

-->

Supports d'ateliers

  <div class="entry" style="margin-bottom:15px;">
  {% for lab in site.data.arduinolabs %}
    <li>
      <a href="/le-petit-algonaute/assets/workshop/arduino/labs/{{ lab.url }}/Guide.pdf">
        {{ lab.title }}
      </a>
    </li>

  {% endfor %}
  </div>
