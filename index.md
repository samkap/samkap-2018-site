---
title: Home
home: true
layout: home
---

Hi! I’m Sam Kapila. I’m a designer and educator living in Austin, TX. I write and speak about Responsive Web Design, Diversity and Inclusion in Tech, and design research and process. 

I’m the Director of Academic Operations and Diversity at [The Iron Yard](http://www.theironyard.com) and I write a column for [net magazine](http://www.creativebloq.com/search?searchTerm=kapila). I make a lot of [playlists](https://open.spotify.com/user/hamtequila">playlists) and travel a lot. I cook and dine out and <a href="http://www.instagram.com/the_tableaux">photograph</a> it all.


<div class="recent">
<h3> Recent </h3>
<div class="recent-posts">
   {% for post in site.posts limit: 3 %}
    // if the category we want to exclude matches
<article>
 <span class="meta">{{ post.date | date: site.date_format }}</span>
 <a href="{{ post.url | prepend: site.baseurl }}"><h2>{{ post.title }}</h2></a>
 <p>{{ post.content | truncatewords:30 | strip_html }}&nbsp;<a class="read-more" href="{{ post.url | prepend: site.baseurl }}"> {{ site.var_read }}  →</a>
 </p>
</article>
        {% endif %}  
    {% endfor %}
</div>