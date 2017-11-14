---
title: Food
position: 7
layout: page
---

## Food

{% for post in site.posts %}



{% if post.categories contains 'food' %}

[{{ post.title }}]({{ post.url | prepend: site.baseurl }})

<small> • {{ post.date | date: site.date_format }}</small>

 {% endif %} {% endfor %}
