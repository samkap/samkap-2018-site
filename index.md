---
title: Home
home: true
layout: page
---

Hi! I’m Sam Kapila. I’m a designer and educator living in Austin, TX. I write and speak about Responsive Web Design, Diversity and Inclusion in Tech, and design research and process. 

I’m the Director of Academic Operations and Diversity at [The Iron Yard](http://www.theironyard.com) and I write a column for [net magazine](http://www.creativebloq.com/search?searchTerm=kapila). I make a lot of [playlists](https://open.spotify.com/user/hamtequila">playlists) and travel a lot. I cook and dine out and <a href="http://www.instagram.com/the_tableaux">photograph</a> it all.
</div><div class="recent">
{% for post in site.posts limit: 3 %}
 {% unless post.next %}<h3>{{ post.date | date: '%Y' }}</h3>
{% else %}{% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}{% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
{% if year != nyear %}<h3>{{ post.date | date: '%Y' }}</h3>{% endif %}
{% endunless %}
 {% if post.categories contains "clips" %}
 {% else if %}
<article>
<p><a href="{{ post.url }}">{{ post.title }}</a> • <small>{{ post.date | date: site.date_format }}</small></p>
</article>
 {% endif %}  
 {% endfor %}
