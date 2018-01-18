---
title: Clips
permalink: "/clips/"
position: 1
layout: page
---

## Shorter notes, links, and thoughts. This is where I collect, where I organize, and where I think.

<div class="clips-group">
{% assign clips = site.clips | reverse %}
{% for post in clips  %}


<article>
<small>  {{ post.date | date: site.date_format }}</small>
<h4><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h4>
<p>{{ post.content | truncatewords:30 | strip_html }}</p>
</article>
  {% endfor %}
</div>

<style>
.clips-group article {
  margin-bottom: 3em;
}
.clips-group article h4 a {
  text-decoration: none;
}
</style>
