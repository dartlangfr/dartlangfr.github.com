---
layout: page
title: Bienvenue sur Dartlangfr.net!
tagline: Site de la communauté française du langage Dart
---
{% include JB/setup %}

Bienvenue sur le site de la communauté française du langage Dart. Ce site a pour vocation de promouvoir ce langage créé par Google.

Nous regroupons sur ce blog toutes les informations concernant les rencontres, les évènements, les conférences autour de Dart, et bien sûr des articles pour parler de technique

Les articles :

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>



