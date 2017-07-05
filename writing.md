---
title: Writing
permalink: "/writing/"
Key: 
layout: page
---

Articles, thoughts, and long-form.

{% for post in site.posts %}
 {% if post.categories == "clips" %}

 {% else if %}
<article>
<p><a href="{{ post.url }}">{{ post.title }}</a></p>
</article>
 {% endif %}  
 {% endfor %}

{% for post in site.posts %}
 {% unless post.next %}<h3>{{ post.date | date: '%Y' }}</h3>
{% else %}{% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}{% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
{% if year != nyear %}<h3>{{ post.date | date: '%Y' }}</h3>{% endif %}
{% endunless %}
{% unless post.category == "clips" or post.category == "food"  %} <p><a href="{{
    post.url | prepend: site.baseurl }}">{{ post.title }}</a><small> • {{ post.date | date:
    site.date_format }}</small></p> {% endunless %} {% endfor %}


