---
title: Clips
permalink: "/clips/"
layout: page
---

## Shorter notes, links, and thoughts. This is where I collect, where I organize, and where I think.

{% for post in site.clips %}
<p><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a><small> • {{ post.date | date: site.date_format }}</small></p>
  {% endfor %}
