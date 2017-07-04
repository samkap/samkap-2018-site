---
title: Writing
permalink: "/blog/"
layout: page
---
<p>Articles, thoughts, and long-form.</p>
  {% for post in site.posts %}
    {% unless post.next %}
      <h3>{{ post.date | date: '%Y' }}</h3>
    {% else %}
      {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
      {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
      {% if year != nyear %}
        <h3>{{ post.date | date: '%Y' }}</h3>
      {% endif %}
    {% endunless %}

   {% unless post.categories == 'clips' %}
    <p><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a><small> • {{ post.date | date: site.date_format }}</small></p>
         {% endif %}
  {% endfor %}
