---
layout: landpage
title: Landpage
date: '2017-12-29 11:30:00 CET'
category: Landpage
published: true
assetsFolder: /le-petit-algonaute/assets/
defaultThumbnail: /le-petit-algonaute/assets/images/blog/thumbmail-empty-150x150.png
---

<h1>
A la Une
</h1>



<table>
  {% for post in site.posts %}
    <tr>
      <td width="150px">
          <a href="{{ post.url | relative_url  }}" ><img style="float:left;" src="{{ post.thumbnail | default: page.defaultThumbnail }}"> </a>
      </td>
      <td>
        <center>
          {% for tag in post.tags %}
            <span style="background-color:#dd6600;font-style:italic;">&nbsp;&nbsp;{{ tag }}&nbsp;&nbsp;</span>&nbsp;&nbsp;
          {% endfor %}
          <br>
          <a href="{{ post.url | relative_url  }}">{{ post.title }}</a>
          <br>
          <small class="post-date" style="color:grey;">{{ post.date | date_to_string }}</small>
        </center>
      </td>
    </tr>
  {% endfor %}
</table>


<!--
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url  }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
-->
