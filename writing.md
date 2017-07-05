---
title: Writing
permalink: "/writing/"
Key: 
layout: page
---

Articles, thoughts, and long-form.

{% for post in site.posts %} {% unless post.next %}

{{ post.date | date: '%Y' }}

{% else %} {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %} {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %} {% if year != nyear %}
{{ post.date | date: '%Y' }}

{% endif %} {% endunless %}
{{ post.title }} • {{ post.date | date: site.date_format }}

{% endfor %}