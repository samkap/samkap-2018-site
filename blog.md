---
title: Writing
permalink: "/blog/"
layout: page
---

Articles, thoughts, and long-form.

{% for post in site.posts %}
{% unless post.category == "clips" %}
    <p><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a><small> • {{ post.date | date: site.date_format }}</small></p>
{% endunless %}
  {% endfor %}
