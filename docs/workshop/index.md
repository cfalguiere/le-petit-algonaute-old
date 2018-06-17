---
layout: section
title: Ateliers
date: '2017-12-27 10:30:00 CET'
tags: ['Atelier']
published: true
assetsFolder: /le-petit-algonaute/assets/workshop
---

{% for workshop in site.data.workshops %}
<div style="width:150px;height:275;margin-right:5px;margin-bottom:5px;float:left;background-color:#dddddd;">
  <div style="width:150px;height:150px;">
    <a alt="{{ workshop.title }}" href="{{ workshop.url }}/"><img src="{{page.assetsFolder}}/{{ workshop.logo }}" /></a>
  </div>

  <div style="width:140px;height:125px;padding:5px 5px 5px 5px;">
    <p style="color:black;font-family:Verdana;text-align: center;">
      {{ workshop.description }}
    </p>
  </div>
</div>
{% endfor %}

<div style="clear: both;">
</div>
